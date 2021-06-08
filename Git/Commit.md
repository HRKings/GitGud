# GitGud: Commit Submodel

**Table of Contents:**

- [GitGud: Commit Submodel](#gitgud-commit-submodel)
	- [1 - Best Practices](#1---best-practices)
	- [2 - Commit Message Model](#2---commit-message-model)
		- [1.1 - Tag](#11---tag)
			- [1.1.1 - Tag Convention](#111---tag-convention)
		- [1.2 - Flag](#12---flag)
			- [1.2.1 - Flag Convention](#121---flag-convention)
		- [1.3 - Subject](#13---subject)
			- [1.3.1 - Subject Convention](#131---subject-convention)
		- [1.4 - Body](#14---body)
			- [1.4.1 - Body Convention](#141---body-convention)
		- [1.5 - Footer](#15---footer)
			- [1.5.1 - Footer Convention](#151---footer-convention)
	- [3 - An example of a good commit message](#3---an-example-of-a-good-commit-message)

---

This submodel aims to provide best practices, naming conventions and guidelines about commits, as they are the essence of Git. It also aims to ease automation of changelogs.

## 1 - Best Practices

Commits are a snapshot of your repository in any given time, serving as a way to get back into a previous version if you need to, for example, if your code breaks. So, two best practices apply on them:

- **Make small commits**, instead of waiting for too many changes to be made, this will ensure that you can go back in time if needed without compromising your code or losing big chunks of changes. 
  - Small commits will also help understanding the history of the repository. Imagine a commit labeled *"Added method1"* and you open it to see the changes and you discover that it actually adds 10 methods, it's not a pleasant surprise.
  - GitGud Flow will help you in this, and its explained [here](../Flow/GitGud_Flow.md)

- **Make good commit messages**, this is a longer topic that will be discussed in the subsection bellow.

## 2 - Commit Message Model

Commit messages are short descriptions of the changes you made in the commit.

Writing good ones will ensure that you and the people that collaborate in a project can keep track of the commit history and understand exactly what changes were made.

Obs.: Use your personal projects as a learning, write good commit messages and you will get used to it.

The default template provided by this submodel is the following:

```Markdown
[tag]{flag (optional)} Subject
~~~
Body (Optional)
~~~
Footer (Optional)
```

### 1.1 - Tag

Tags are usually the first thing in a commit message, they hit to what the commit is about, and ease searching later.

Tags and their usage cases:

- `[feature]` : A new feature and small additions;
- `[change]` : Any changes on existing functionality;
- `[fix]` : A bugfix or hotfix;
- `[style]` : Any change in styling, layout, css, design, etc.;
- `[refactor]` : Any code refactoring, cleanup, formatting, improvements in code style and readability;
- `[test]` : Adding, changing or refactoring tests, with no production code change;
- `[docs]` : Changes in documentation, readme, guides, etc.;
- `[chore]` : Updates/Removes/Adds dependencies, package manager configs, build tasks, etc;
- `[misc]` : Anything not covered by the above categories.
- `[merge]` : Special tag used only when merging pull requests, mainly used by the [Flow Submodel](../Flow/GitGud_Flow.md).

#### 1.1.1 - Tag Convention

- Tags goes before everything;
- Tags need to be encased in square brackets `[]`;
- They are always written in lower case.

### 1.2 - Flag

Flags are short symbols or abbreviations that help understand better the code or to take precautions when pulling this changes.

Flags and their usages:

- `{!!!}` : *Breaking change* - Significant changes in software architecture and/or logic, that affects existing code. **If present, needs to be the first flag**;
- `{db}` : Changes that require database structure or data to be updated;
- `{api}` : Changes that modify the API usage, models or structure.
- `{ux}` : Change in user experience - Anything that needs the user to relearn to use a feature;
- `{dpc}` : *Deprecated* - Commits with this flag deprecates existing code;
- `{rm}` : *Code Removal* - Means that this commit removes old/legacy/deprecated code;
- `{wip}` : *Work In Progress* - All commits related to a feature/change will have this flag, and will only be removed when the final version of a feature/change is available. Commits marked as WIP can never be merged.

#### 1.2.1 - Flag Convention

- Flags goes after the tag;
- The flags section need to be encased in curly braces `{}`;
- Flags are always written in lowercase;
- If multiple flags are present, they need to be separated by a slash `/`.

Example of tag usage:

```XML
[feature]{!!!/ux/db/api/wip} Commit message here
[chore]{ux/db/api} Commit message here
[feature]{wip} Commit message here
[feature]{!!!/db} Commit message here
[style]{ux/wip} Commit message here
[feature]{!!!} Commit message here
```

### 1.3 - Subject

This is the line that will show in the commit history, and contains a short descriptive message about the changes.

#### 1.3.1 - Subject Convention

- The subject is always the first line of the commit message;
- It shout be around 50 characters but with a limit of 80;
- It should begin with a capital letter and be written in the imperative (eg.: **"Add"** instead of *"Added"* or *"Adds"*).

### 1.4 - Body

The body is an optional section where you can offer a more detailed description of the commit, while there is no real limit, keep it short, around 100 characters.

#### 1.4.1 - Body Convention

- The body should be separated of the subject by one line containing three tildes `~~~`;
- It shout be wrapped in about 100 characters.

### 1.5 - Footer

The footer is optional and used when a issue/bug tracker is used. It is used to reference/close an bug/issue ID.

#### 1.5.1 - Footer Convention

- The footer is only used when a issue/bug tracker is in use on the project;
- It should be separated from the body or subject by one line containing three tildes `~~~`;
- If a issue/bug is closed, then its ID should be put after a "Closes: " message, and
	- For example: *Closes: #123* or *Closes: #123, #456*
- If a issue/bug is referenced, then its ID should be put after a "See also: " message
	- For example: *See also: #123* or *See also: #123, #456*
- Multiple IDs need to be comma `,` separated
- IDs need to be prefixed with a hash `#`

## 3 - An example of a good commit message

```XML
[feature]{!!!}{wip} Around 50 characters to a 80 limit
~~~
More detailed explanatory text, wrapped in about 100 characters. Separated by one line containing three tildes `~~~`
~~~
Closes: #123
See also: #456, #789
```

Or more conventional and practical examples:

```Markdown
[docs] Fix typo in README.md
```

```Markdown
[feature]{!!!}{api} Add new api call
~~~
Closes: #123
```
