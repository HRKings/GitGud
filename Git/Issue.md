# GitGud: Issue Sub-Model

**Table of Contents:**

- [GitGud: Issue Sub-Model](#gitgud-issue-sub-model)
	- [1 - Issue Template Structure](#1---issue-template-structure)
		- [1.1 - Title](#11---title)
			- [1.1.1 - Tag](#111---tag)
			- [1.1.2 - Flags](#112---flags)
		- [1.2 - Description](#12---description)
		- [1.3 - Logs](#13---logs)
		- [1.4 - How to reproduce](#14---how-to-reproduce)
		- [1.5 - Additional Info](#15---additional-info)
	- [2 - Issues as todo lists for the team](#2---issues-as-todo-lists-for-the-team)
	- [3 - Responding issues](#3---responding-issues)

---

Issue Trackers are one of the most useful features of a Git platform that you may be using, it enables end-users and other developers to create formal reports of bugs, issues and to-dos in the repository.

If you choose to use the GitGud Issue Model, you **must** provide a template for people that can open tickets in the issue tracker. This helps people know how to provide the necessary information about the issue for the developers to resolve them.

## 1 - Issue Template Structure

While is best to provide your own template, here is a default structure of one that can be tweaked to your needs.

```Markdown
# [tag (optional)]{flag (optional)} Title

Description

## Logs

## How to reproduce

## Additional Info
```

### 1.1 - Title

The title is a short description of the issue, it is what everyone will see first, so keep it descriptive.

You may have notice that the *tag* and *flag* fields in the template are optional. That is because is best to use the labeling tools provided by your platform, but is also something nice to have, as it helps narrow down search results for instance.

#### 1.1.1 - Tag

Tags are the "category" that the issue will fall into, and it's best for you to create ones that suits your project, but here are some basic ones that you can use as reference.

- `[bug]` : A bug/issue report;
- `[todo]` : A tracking report for any changes that needs to be done by the team;
- `[misc]` : Anything not covered by the above category.

#### 1.1.2 - Flags

Flags are subcategories that help refine searches. The same concept above about creating them applies here.

- `{db}` : Issues about database or data modeling;
- `{api}` : Issues about the API and it's usage;
- `{ux}` : Issues about user experience;

### 1.2 - Description

The description is detailed, and covers how the issue happened and what it caused. Be as descriptive as possible.

### 1.3 - Logs

Here is where you put any crashlog, log or report created by the software. Any log must not be posted directly here, instead it needs to be put in a pasting service (like pastebin or gist) and its link be put here.

### 1.4 - How to reproduce

The How to Reproduce section is where you describe how the issue can be replicated by other people. It helps developers to pinpoint the issue origin faster. Create a numbered list here with the steps to reproduce the issue.

### 1.5 - Additional Info

Additional info can be anything, image links showing the issue, related issues, video links or anything like that. But only post relevant information for the issue.

## 2 - Issues as todo lists for the team

Issues can be used as todo lists for the developers working on a feature, this is a good thing because you can close the issue with a commit or pull request. You can also create checklists of the steps of features that needs to be implemented.

## 3 - Responding issues

Responding issues is often a necessary thing. Ask for more information or explain some steps that can lead the user to fix the issue without the need of a code change. Issues are a good place to discuss about changes with other developers. Just remember:

- Be peaceful. Discuss in a manner that will help to achieve a solution.
- If there is growing confusion or debate, ask yourself if written word is still the best form of communication. Talk virtually face-to-face, invite people to a voice call and at same time post a follow-up to summarize any discussion made outside the original platform, this is useful for other who are following along, now or in the future.
- Be aware of negative bias when writing, we assume a negative tone when the content is neutral. Keep a positive language as opposed to neutral.
- If comfortable, use emoji or emoticons. It helps making your comment more expressive and avoid negative or neutral content. And it helps to give a moral boost to the author of the issue.