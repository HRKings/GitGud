# The Commit

Commits are an essential part of Git, and this session will guide you through some practices about them.

The first thing that you need to understand about commits is that they are a snapshot of your repository in any given time, serving as a way to get back into a previous version if you need to, for example, if your code breaks.

**Make small commits**, instead of waiting for too many changes to be made, this will ensure that you can go back in time if needed without compromising your code or losing big chunks of changes.

Small commits will also help understanding the history of the repository. Imagine a commit labeled *"Added method1"* and you open it to see the changes and boom, you discover that it actually adds 10 methods, it's not a pleasant surprise.

GitFlow will help you in this, and its explained [here](Git_Flow.md)

**Make good commit messages**, this is a longer topic that will be discussed in the subsection bellow.

## 1 - How to make a good commit message

Commit messages are short descriptions of the changes you made in the commit.

Writing good ones will ensure that you and the people that collaborate in a project can keep track of the commit history and understand exactly what changes were made.

Obs.: Use your personal projects as a learning, write good commit messages and you will get used to it.

One good structure for commit messages are:

```Markdown
tag/flag : Subject

Body (Optional and not needed in this model)

Footer (Optional)
```

### 1.1 - Tags

Tags are usually the first thing in a commit message, they hit to what the commit is about, and ease searching later.

Tags and their usage cases:

- `feature` : A new feature and small additions;
- `fix` : A bugfix or hotfix
- `style` : Any change in styling, layout, css, etc.;
- `refactor` : Any code refactoring, cleanup, formatting, improvements in code style and readability;
- `test` : Adding, changing or refactoring tests, with no production code change;
- `docs` : Changes in documentation, readme, guides, etc.;
- `chore` : Updating dependencies, package manager configs, build tasks, etc;
- `misc` : Anything not covered by the above categories.

**Structure:**

- Tags goes before everything;
- Tags need to be encased in square brackets `[]`;
- They are always written in lower case.

### 1.2 - Flags

Flags are indicatives that help understand better the code or to take precautions.

Flags and their usages:

- `!!!` : *Breaking change* - Significant changes in software architecture and/or logic, that affects existing code. **If present, needs to be the first flag**;
- `db` : Changes that require database structure or data to be updated;
- `api` : Changes that modify the API usage, models or structure.
- `ux` : Change in user experience - Anything that needs the user to relearn to use a feature;
- `wip` : *Work In Progress* - All commits related to a feature/change will have this flag, and will only be removed when the final version of a feature/change is available. Commits marked as WIP can never be merged.

**Structure:**

- Flags goes after the tag;
- Flags need to be encased in curly braces `{}`;
- Flags are always written in lowercase.

Example of tag usage:

```XML
[feature]{!!!}{ux}{db}{api}{wip} Commit message here
[chore]{ux}{db}{api} Commit message here
[feature]{wip} Commit message here
[feature]{!!!}{db} Commit message here
[style]{ux}{wip} Commit message here
[feature]{!!!} Commit message here
```

### 1.3 - Subject

This is the line that will show in the commit history, and contains a short descriptive message about the changes.

**Structure:**

- The subject is always the first line of the commit message;
- It shout be around 50 characters but with a limit of 80;
- It should begin with a capital letter and be written in the imperative (eg.: **"Add"** instead of *"Addeded"* or *"Adds"*).

### 1.4 - Body

The body is a detailed description of the changes you made and why you made them. Commits usually are not complex enough that they need a body, and they **should not** need one if you are following this model because the changes are small ones at once.

**Structure:**

- The body needs to be separated from the subject by one blank line;
- It needs to start with a capital letter;
- Each line should have no more than 70 characters;
- Bullet points are made with an asterisk `*`;

### 1.5 - Footer

The footer is optional and used when a issue/bug tracker is used. It is used to reference/close an bug/issue ID.

**Structure:**

- The footer is only used when a issue/bug tracker is in use on the project;
- It should be separated from the body or subject by one blank line.

## 2 - An example of a good commit message

```XML
[feature]{!!!}{wip} Around 50 characters to a 80 limit

More detailed explanatory text, wrapped in about 70 characters. Separated by a blank line in the start.

* Bullet lists
* Are nice

Resolves: #123
See also: #456, #789
```

Or more conventional and practical examples:

```Markdown
[docs] Fix typo in README.md
[feature]{!!!}{api} Add new api call. Resolve #123
```
