# How to GitGud Flow

**Table of Contents:**

* [How to GitGud Flow](#how-to-gitgud-flow)
	* [1 - Creating branches](#1---creating-branches)
		* [1.0 - When initialing the repository for the first time](#10---when-initialing-the-repository-for-the-first-time)
		* [1.1 - Creating the Stable branch](#11---creating-the-stable-branch)
			* [1.1.1 - Creating the stable branch on a existing project](#111---creating-the-stable-branch-on-a-existing-project)
		* [1.2 - Creating a Working branch](#12---creating-a-working-branch)
		* [1.3 - Creating a Hotfix branch](#13---creating-a-hotfix-branch)
	* [2 - Publishing a branch](#2---publishing-a-branch)
	* [3 - Merging a working branch](#3---merging-a-working-branch)
		* [3.1 - Merging a Hotfix branch](#31---merging-a-hotfix-branch)
	* [4 - Deleting a branch](#4---deleting-a-branch)

---

This guid lists the commands necessary to use [GitGud Flow](GitGud_Flow.md) from the command line.

## 1 - Creating branches

Creating branches is one of the main thing you will be doing while developing, those are the commands used.

### 1.0 - When initialing the repository for the first time

If you need to initialize your repository for the first time, you can use:

```Bash
git init
git checkout -b master
git add .
git commit -am "[misc] Initial commit"
```

And then create the stable branch.

### 1.1 - Creating the Stable branch

This command creates a Stable branch, and push it to the remote.

```Bash
git checkout -b stable
git push origin stable
```

This will create a stable branch with only one empty commit.

#### 1.1.1 - Creating the stable branch on a existing project

If you already have a project and want to opt for GitGud Flow model, you need to branch the stable from master, using:

```Bash
git checkout master
git checkout -b stable
git push origin stable
```

This will create a stable branch and push it to the remote.

### 1.2 - Creating a Working branch

To create a new working branch and automatically checkout to it, execute this command.

```Bash
git checkout master
git checkout -b TYPE/BRANCH_NAME
```

*Please refer to the [GitGud Flow Guide](GitGud_Flow.md#3---working-branches) for the list of working branches types.*

### 1.3 - Creating a Hotfix branch

The hotfix branch always come from the stable branch or from a versioning one, this being said, you need to execute

```Bash
git checkout stable
git checkout -b hotfix/BRANCH_NAME
```

## 2 - Publishing a branch

When working with other people, you need to make the branch you are working on available on the remote repository.

To make this possible you need to execute:

```Bash
git push -u origin BRANCH_NAME
```

## 3 - Merging a working branch

When working alone in a branch, once you complete all the changes you can merge it directly into Master using the command line.

```Bash
git checkout master
git merge BRANCH_NAME
```

**Disclaimer:** *When working with a team is advised that you always merge via Pull Request.*

### 3.1 - Merging a Hotfix branch

Hotfix branches are special in the sense that they need to be merged both into stable and into master.

```Bash
git checkout stable
git merge hotfix/BRANCH_NAME

git checkout master
git merge hotfix/BRANCH_NAME
```

**Disclaimer:** *When working with a team is advised that you always merge via Pull Request.*

## 4 - Deleting a branch

After you complete a working branch you will need to delete it, doing so is simple as:

```Bash
git branch -d BRANCH_NAME
```
