+++
title = "Critical Bugfix"
date = 2014-01-15T19:49:49+01:00
updated = 2014-01-15T19:49:49+01:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Markus Diem"]
+++

we have found a critical bug which – in some cases – prevents nomacs from starting correctly.
If you experience this issue, we would recommend to update nomacs to version 1.6.3.
 The issue applies only to the Windows versions.
Users of other OS can safely enjoy version 1.6.2.
Sorry for any inconveniences caused.
For the Matlab users who do not enjoy the default image display behavior of Matlab:
this script allows you to directly display images in nomacs.

```matlab
function nomacs(img, varargin)
% nomacs(img, varargin)
% 
% nomacs displays the image img in nomacs
%
% INPUT:
%   img         the image to display
% 
%   normalize   displays the image in the range between [val1 val2]. If the
%               parameter is set to [] the image is normalized between
%               min(img(:)) and max(img(:)). Note: It is possible to pass
%               the following parameter struct as a second parameter, if
%               normalization should not be performed.
%   
%   tempFolder  the folder where the image is saved temporary (it is
%               deleted afterwards
%
%   exePath     specify the exePath if it is not in Program Files (x86)

if isempty(img)
    return;
elseif size(img,4) > 4
    warning('NOMACS:falseImg', ['The number of channels must not be '...
        'greater than four.']);
    return;
end

p = parse_inputs(varargin{:});

% check if nomacs is up & running
if ~exist(strrep(p.exePath, '"', ''), 'file')
    display( p.exePath);
    error('NOMACS:notFound', ['Sorry, I could not locate nomacs.exe \n'...
        'Please specify the correct exePath.']);
end

if isfield(p, 'normalize')
    
    if isempty(p.normalize)
        
        img = im2double(img);
        img = img-min(img(:));
        img = img./max(img(:));

    elseif length(p.normalize) == 2
        n = p.normalize;
        img = double(img);
        img = img-n(1);
        img = img./(n(2) - n(1));        
    end
end

imwrite(img, p.tempFolder);

if ~isunix
    system([p.exePath ' ' p.tempFolder ' &']);
else
    unix([p.exePath ' ' p.tempFolder ' &']);
end

delete(p.tempFolder);

%-------------------------------------------------------------------------
%   Subfunction: Parse Inputs
%-------------------------------------------------------------------------
function params = parse_inputs(varargin)

% called with normaliztion only
if nargin == 1 && isfloat(varargin{1})
    params.normalize = varargin{1}; 
% second param is the struct
elseif nargin == 1 && isstruct(varargin{1})
    params = varargin{1};
% three parameters (img, [], p)
elseif nargin == 2 && isfloat(varargin{1}) && isstruct(varargin{2})
    params = varargin{2};
    params.normalize = varargin{1};
% no params
elseif nargin == 0
    params = [];
else
    warning('NOMACS:paramFalse', ['The input parameters do not'...
        ' conform to the required schema. Using default parameters'...
        ' instead.']);
end

if ~isunix
    
    try
        exename = winqueryreg('HKEY_LOCAL_MACHINE', 'SOFTWARE\Microsoft\Windows\CurrentVersion\App Paths\nomacs.exe');
    catch
        exename = fullfile('C:', 'Program Files (x86)','nomacs', 'nomacs.exe');
    end
    imgname = fullfile(tempdir, 'matlab-nomacs.tif');
else
    exename = '';   % TODO
    imgname = '';   % TODO
end

% define vars
default_params.exePath          = ['"' exename '"'];
default_params.tempFolder       = imgname;

params = merge_structs(params, default_params);


%-------------------------------------------------------------------------
%   Subfunction: Merge Structs
%-------------------------------------------------------------------------
function struct2 = merge_structs(struct1, struct2)
% function new_struct = merge_structs(struct1, struct2)
%
%   Merges both STRUCTs.
%   All values where both structs have the same fieldnames are taken from
%   STRUCT1. The NEW_STRUCT contains the fields of both STRUCTS.


if isempty(struct1)
    return;
end

names = fieldnames(struct1);

for i = 1:length(names)
    struct2.(names{i}) = struct1.(names{i});
end
```

— the nomacs team
