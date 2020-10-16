# How to GitGud Flow

**Table of Contents:**

- [How to GitGud Flow](#how-to-gitgud-flow)
	- [1 - Creating branches](#1---creating-branches)
		- [1.1 - Creating the Stable branch](#11---creating-the-stable-branch)
			- [1.1.1 - Creating the stable branch on a existing project](#111---creating-the-stable-branch-on-a-existing-project)
		- [1.2 - Creating a Working branch](#12---creating-a-working-branch)
		- [1.3 - Creating a Hotfix branch](#13---creating-a-hotfix-branch)
	- [2 - Publishing a branch](#2---publishing-a-branch)
	- [3 - Merging a working branch](#3---merging-a-working-branch)
		- [3.1 - Merging a Hotfix branch](#31---merging-a-hotfix-branch)
	- [4 - Deleting a branch](#4---deleting-a-branch)

---

This guid lists the commands necessary to use [GitGud Flow](GitGud_Flow.md) from the command line.

## 1 - Creating branches

Creating branches is one of the main thing you will be doing while developing, those are the commands used.

### 1.1 - Creating the Stable branch

This command creates an empty Stable branch, and push it to the remote.

```Bash
git checkout --orphan stable
git commit --allow-empty -m "[misc] Stable branch start"
git push origin stable
```

This will create a stable branch with only one empty commit.

#### 1.1.1 - Creating the stable branch on a existing project

If you already have a project and want to opt for GitGud Flow model, you need an empty stable branch, you can create one using:

```Bash
git checkout --orphan stable
git rm -rf .
git commit --allow-empty -m "[misc] Stable branch start"
git push origin stable
```

This will create a stable branch, remove any staged files, create an empty commit and push it to the remote.

### 1.2 - Creating a Working branch

To create a new working branch and automatically checkout to it, execute this command.

```Bash
git checkout master
git checkout -b type/branch_name
```

*Please refer to the [GitGud Flow Guide](GitGud_Flow.md#1---the-premise) for the list of working branches types.*

### 1.3 - Creating a Hotfix branch

The hotfix branch always come from the stable branch or from a versioning one, this being said, you need to execute

```Bash
git checkout stable
git checkout -b hotfix/branch_name
```

## 2 - Publishing a branch

When working with other people, you need to make the branch you are working on available on the remote repository.

To make this possible you need to execute:

```Bash
git push -u origin branch_name
```

## 3 - Merging a working branch

When working alone in a branch, once you complete all the changes you can merge it directly into Master using the command line.

```Bash
git checkout master
git merge branch_name
```

**Disclaimer:** *When working with a team is advised that you always merge via Pull Request.*

### 3.1 - Merging a Hotfix branch

Hotfix branches are special in the sense that they need to be merged both into stable and into master.

```Bash
git checkout stable
git merge hotfix/branch_name

git checkout master
git merge hotfix/branch_name
```

**Disclaimer:** *When working with a team is advised that you always merge via Pull Request.*

## 4 - Deleting a branch

After you complete a working branch you will need to delete it, doing so is simple as:

```Bash
git branch -d branch_name
```
