# The Changelog

**Table of Contents:**

- [The Changelog](#the-changelog)
	- [1 - The changelog structure](#1---the-changelog-structure)
		- [1.1 - Title](#11---title)
		- [1.2 - Body](#12---body)
		- [1.3 - Unreleased Section](#13---unreleased-section)
		- [1.4 - Headline (Version and Date)](#14---headline-version-and-date)
		- [1.5 - Added Section](#15---added-section)
		- [1.6 - Changed Section](#16---changed-section)
		- [1.7 - Updated Section](#17---updated-section)
		- [1.8 - Deprecated Section](#18---deprecated-section)
		- [1.9 - Removed Section](#19---removed-section)
		- [1.10 - Fixed Section](#110---fixed-section)
		- [1.11 - Issues Section](#111---issues-section)
	- [2 - Convention](#2---convention)
	- [3 - Flags](#3---flags)

Changelogs are human-readable files created to keep track of notabel changes in each release.

In the GitGud model (mainly in the [GitGud Flow](../Flow/GitGud_Flow.md)), changelogs are required each time a new branch are merged in one of the versioning branches and they need to follow the [Versioning Model](Versioning_Guide.md).

This model is a modification of the [Keep a Changelog](keepachangelog.com/), all will try to integrate any changes made to the original document.

## 1 - The changelog structure

The changelog are structured as follows:

```Markdown
# Title

{[Previous release](LINK_HERE)}

Body

## [Unreleased]

## [VERSION_TAG] {RELEASE_DATE}

### Added

### Changed

### Updated

### Deprecated

### Removed

### Fixed

### Issues
```

### 1.1 - Title

The title is required, but if you don't want to think about a title, simply put `Changelog` as a title in its place.

You can also put a cool release name like: `Canary Version`, limits this to your imagination.

### 1.2 - Body

The body is a brief explanation of what this release holds or for what this changelog is, why it was made or a general message to the public or other team members.

This message can be, for example, an explanation of what will break, and if an API or Database will suffer significant changes or will need to be rebuilt.


Keep it short, all the changes should be described in the changelog, not in the body.

The body could also contain a link to a previous changelog, if they are split in one changelog file per release.

### 1.3 - Unreleased Section

The `[Unreleased]` section, holds any changes that are still Work In Progress, they are yet to be released.

You keep here all notable changes that you want people to expect.

Other than that, when those changes are ready you can just move them to other section.

### 1.4 - Headline (Version and Date)

This is the entry point for the changelog, is labeled in the template as `[VERSION_TAG] (DATE)`, where you replace *VERSION_TAG* with the actual version tag of this release and the *DATE* with the date when the released was made.

### 1.5 - Added Section

This is a section reserved for new additions and features

### 1.6 - Changed Section

Keep here all the changes in existing functionality.

### 1.7 - Updated Section

Here is where you will list any updates to dependencies, frameworks, etc.

### 1.8 - Deprecated Section

List here all features and functionalities that will be removed soon. Usually what gets deprecated, gets removed in the next release.

### 1.9 - Removed Section

Here will be all features and functionality that was removed in this release.

### 1.10 - Fixed Section

This section hold any issues that were fixed in this release.

### 1.11 - Issues Section

List in here any issue found in this release that will be patched, security vulnerabilities, yet-to-be fixed bugs and potential issues that people could encounter when using this release.

## 2 - Convention

- All of the entries inside the sections needs to be in a bullet list form, using the hyphen (`-`) as the list marker.

- After the hyphen, you can put flags (if any)

- After any present flag, the entry needs to start with an capitalized letter.

- If the changelog, contains multiple versions, the latest needs to come first.

- Empty sections cannot appear in the changelog.

- The date is in the ISO standard (YEAR-MONTH-DAY)

## 3 - Flags

Flags are very useful, they reflect some information to the people reading the changelog beforehand.

The flags are:

- `{!!!}` : *Breaking change* - Significant changes in the release architecture and/or logic, that affects existing releases. **If present, needs to be the first flag**;
- `{DB}` : Changes that require database structure or data to be updated;
- `{API}` : Changes that modify the API usage, models or structure.
- `{UX}` : Change in user experience - Anything that needs the user to relearn to use a feature.

These flags helps the person reading the code to find what the entry will do to existing releases.
