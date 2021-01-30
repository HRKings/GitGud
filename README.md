# GitGud : A modular Git model

**Table of Contents:**

* [GitGud : A modular Git model](#gitgud--a-modular-git-model)
	* [What is a submodel](#what-is-a-submodel)
	* [History](#history)
	* [Reasons to use GitGud](#reasons-to-use-gitgud)
	* [Submodels](#submodels)
	* [Badges](#badges)

----

Git, without doubt is one of the greatest development tools in existence, but using the right way is a difficult thing, while you can search the internet for articles and various models, you can start getting a lot of tabs open and many models to follow and opt-in. With this problem in mind that we created the GitGud Model, it covers everything, from commit messages to changelogs. You can chose to use only one of the submodels or all of them, or even create your own guidelines based on it, the choice is yours.

## What is a submodel

A submodel is a collection of guidelines, code of conducts and naming conventions. This collection, when focused in a specific topic, creates a model that can be used in an independent way or together with other models, hence the nomenclature submodel, as is just a part of a larger one.

## History

When using git, we ended up with multiple tabs listing various guidelines and models, that provided only pieces of the information that we wanted. In the end we needed to choose a few points of each article that we found and twet it to our linking.

That is why we created the GitGud Model, to be a centralized place to gather all this info and create a concise and comprehensive model that we can update over time to create a really easy and powerful way of using Git and its features. And of course, it's open source as everyone can contribute with their ideas and changes, and of course, tweak the model and its submodels to best suit their projects.

## Reasons to use GitGud

- Reduces the effort to understand and read documentation and code;
- Provides a template on how to use Git features (commits, pull requests, etc.);
- Reduces the amount of necessary discussion between team members over trivial Git things;
- Improves code and commit history quality;
- Ease the use of CI/CD;
- Facilitates code collaboration.

----

## Submodels

- [GitGud: Commit Submodel](Git/Commit.md) - Commit rules and commit messages convention
- [GitGud: Pull Request Submodel](Git/Pull_Request.md) - Pull Requests convention and best practices
- [GitGud: Issue Submodel](Git/Issue.md) - Issues guidelines and templates

**GitGud Flow:**

- [GitGud Flow Submodel](Flow/GitGud_Flow.md) - An easy branching model focused CI/CD and collaboration
  - [GitGud Flow Commands Guide](Flow/GitGud_Flow_HowTo.md) - How to follow the GitGud Flow from the command line

**Versioning:**

- [GitGud: Versioning Submodel](Versioning/Versioning.md) - An easy versioning model based on the *Semantic Versioning*
- [GitGud: Changelog Submodel](Versioning/Changelog.md) - An easy changelog model based on the *Keep a Changelog*

----

## Badges

If you plan to use the GitGud Model, you can put a badge somewhere in your documentation, *README* or *CONTRIBUTING*, to show that you are using the model or the submodels.

Some examples:

[![GitGud](https://img.shields.io/badge/GitGud-v1.0-red?style=flat-square)](https://github.com/HRKings/GitGud/tree/stable)

```Markdown
[![GitGud](https://img.shields.io/badge/GitGud-v1.0-red?style=flat-square)](https://github.com/HRKings/GitGud/tree/stable)
```

[![GitGud Versioning](https://img.shields.io/badge/GitGud|Versioning-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Versioning/Versioning.md)

```Markdown
[![GitGud Versioning](https://img.shields.io/badge/GitGud|Versioning-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Versioning/Versioning.md)
```

[![GitGud Changelog](https://img.shields.io/badge/GitGud|Changelog-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Versioning/Changelog.md)

```Markdown
[![GitGud Changelog](https://img.shields.io/badge/GitGud|Changelog-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Versioning/Changelog.md)
```

[![GitGud Flow](https://img.shields.io/badge/GitGud|Flow-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Flow/GitGud_Flow.md)

```Markdown
[![GitGud Flow](https://img.shields.io/badge/GitGud|Flow-v1.0-blue?style=flat-square)](https://github.com/HRKings/GitGud/blob/stable/Flow/GitGud_Flow.md)
```
