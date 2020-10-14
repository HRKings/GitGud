# The GitGud Flow

**Table of Contents:**

- [The GitGud Flow](#the-gitgud-flow)
	- [1 - The Premise](#1---the-premise)
		- [1.1 - Stable](#11---stable)
		- [1.2 - Master](#12---master)
		- [1.3 - WIP](#13---wip)
		- [1.4 - Fix](#14---fix)
		- [1.5 - Task](#15---task)
		- [1.6 - Hotfix](#16---hotfix)
		- [1.7 - Optional Versioning Branches](#17---optional-versioning-branches)

GitGud Flow is a branching model that helps maintaining your code clean and reliable in case of something breaking. This document will guide you in using the GitGud Flow and the commands involved, remember that this only a model and you can use this only as a document.

GitGud flow is heavily based from the standard Git Flow, but with some differences. First of all, it is a lot simpler. You merge into master directly and then use another branch to CD. Some naming was also changed to make it more broader and comprehensive.

**Disclaimer:** This guide use the [Commit Guide](../Topics/Commit.md) and the [Pull Request Guide](../Topics/Pull_Request.md) from GitGud. Use them as a base anytime it references any of these two features.

## 1 - The Premise

When using the Git Flow you need to understand what you can do and how it works.

Here is the list of branch types in GitGud Flow:

**Permanent branches:**

- *Stable*
- *Master*

**Working branches:**

- WIP
- Fix
- Task
- Hotfix

Remember that those are only the types of the branches, but the naming is up to you.

The basic working of this flow is:

1. You branch of the master branch;
2. You make modifications;
3. You merge back into master branch once is ready;
4. You then merge master branch into the stable branch once all the changes are complete.

Bellow is a more detailed explanation of what are those types and how to use the branches.

### 1.1 - Stable

This is your release ready branch, here will be only the latest production ready changes.

**General Rules:**

- You only have one stable branch;
- **You never commit directly to this branch;**
- This branch is never deleted;

**Merging Rules:**

- You only merge from master, once all the changes from a version are ready;
- You can only merge hotfix branches;
- When merging, you should make a Pull Request with a changelog and squash the commits.

**Naming:**

- Lower case;
- Snake case;
- Descriptive and clear that it is only for stable code.

### 1.2 - Master

This branch is where all the development progress will be made, all features, fixes and changes will go here.

**General Rules:**

- You only have one master branch;
- It's not advised to commit directly in this branch;
- This branch is never deleted;
- This is your repository default branch.

**Merging Rules:**

- You only merge complete wip branches;
- You can merge any fix;
- You can merge any task branch;
- When merging you should make a Pull Request with a changelog.

**Naming:**

- Lower case;
- Snake case;
- This can be anything you want, and usually is left to the git into default.

### 1.3 - WIP

The most used of them all, is where you test new features, change or update things.

**General Rules:**

- You can have multiple wip branches;
- WIP branches are deleted after they are merged into the development branch;
- You can commit freely and test in them at will.

**Merging Rules:**

- You will only merge a complete wip branch to the master branch.

**Naming:**

- Lower case;
- Snake case;
- Prefixed with `wip/`;
- Descriptive and clear of its purpose, be a new feature or a change.

### 1.4 - Fix

Fix branches are used to fix bugs, missing resources found in the master branch. Mainly used for uncaught issues in tests or runtime issues not detected in the development.

**General Rules:**

- You can have multiple bugfix branches;
- Fix branches are deleted after they are merged into the master branch;
- You can fix more than one bug on the branch.

**Merging Rules:**

- You will only merge a complete fix branch in the development branch.

**Naming:**

- Lower case;
- Snake case;
- Prefixed with `fix/`;
- Descriptive and clear of its purpose. What are you fixing ?

### 1.5 - Task

This type of branch is only used when updating dependencies, frameworks, build tasks and other updates required.

**General Rules:**

- You can have multiple task branches;
- Task branches are deleted after they are merged into the development branch;
- You can only make commits related to tasks.

**Merging Rules:**

- You will only merge a complete task branch that has passed all tests to the master.

**Naming:**

- Lower case;
- Snake case;
- Prefixed with `task/`;
- Descriptive and clear of its purpose. What task are you doing ? Updating some dependency ? Documentation ?

### 1.6 - Hotfix

This branch is a priority fix, when you find a serious bug in the stable branch that needs to be resolved as soon as possible, you commit to a hotfix branch to resolve it.

**General Rules:**

- Hotfix branches are based of the stable branch;
- Hotfix branches are deleted after they are merged into the stable branch;

**Merging Rules:**

- After the hotfix is complete, you merge it to stable and master branches.

**Naming:**

- Lower case;
- Snake case;
- Prefixed with `hotfix/`;
- Descriptive and clear of its purpose.

### 1.7 - Optional Versioning Branches

Those are branches that are not present in the model, but can be used if needed. For example:

- A beta branch;
- A public_test branch.

All the rules from the stable branch applies here.
