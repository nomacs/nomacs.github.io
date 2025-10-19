+++
title = "How to Contribute"
description = "Contribute to nomacs or improve documentation."
date = 2021-05-01T18:10:00+00:00
updated = 2021-05-01T18:10:00+00:00
draft = false
weight = 410
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = ""
toc = true
top = false
+++

The best way to improve nomacs is your contribution.
You can submit simple changes such as formatting corrections,
extend manuals and READMEs where appropriate,
[translate nomacs](https://github.com/nomacs/nomacs/blob/master/ImageLounge/manuals/Translation.md),
fix bugs, or submit new features.

Make sure to read the [Code of Conduct](../code-of-conduct/).

## Create an issue

- [Bug report](https://github.com/nomacs/nomacs/issues/new?template=bug_report.md)
- [Feature request](https://github.com/nomacs/nomacs/issues/new?template=feature_request.md)

## Improve documentation

The documentation lives in [`nomacs.gitbub.io` repository](https://github.com/nomacs/nomacs.github.io).

## Contribute code

If you contribute source code, you should fork and then clone nomacs:

```git
git clone git@github.com:your-username/nomacs.git
```

- Build nomacs on your machine.
- Make your changes.
- Commit in small chunks (one feature/bug fix per commit).
- Push to your fork and submit a pull request.

We will comment on pull requests within one week. Here are some things that increase the chances of your PR being accepted:

- Write good commit messages.
- Follow our style guide.
- Pass all the Github action checks.

### Style

nomacs might have a weird coding style at the first glance, however we try to follow at least some rules:

- `using namespace` is prohibited (even for `std`)
- Naming
  - Class names start with a capital letter (i.e. `DkBaseManipulator`).
  - Methods start with lowercase (i.e. `name()`).
  - Prefix members with an m (i.e. `int mAction = 0`).
  - Prefix classes with `Dk`.
- format C++ sources with `clang-format -i --style=file your_contribution.cpp`
- Encapsulate everything with the namespace `nmc`

Right:

```cpp
namespace nmc
{

class DllCoreExport DkBaseManipulator
{
public:
    DkBaseManipulator(QAction *action = 0);

    QString name() const;

private:
    QAction *mAction = 0;
};

}
```

Wrong:

```cpp
class DllCoreExport baseManipulator
{

public:
  baseManipulator(QAction* Action = 0);

  QString Name() const;

private:
  QAction* action = 0;
};
```
