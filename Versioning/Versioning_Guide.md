# Versioning

This versioning guide is only an explanation of the [Semantic Versioning](https://semver.org) and is only used as a quick reference. If you want to hare more details, head to SemVer website to read more.

## 1 - Basic Versioning

Basic versioning is done in the form of: `MAJOR.MINOR.PATCH`, where:

- MAJOR version is when you make changes that are incompatible with a previous version;
- MINOR version is when you add functionality in a backwards compatible manner;
- PATCH version is when you make backwards compatible bug fixes.

Where backwards compatible means that a user using a previous version can still use and interact with services provided in the current versions, for example:

- In a game, it will not break saves or corrupt data
- In a software, it will still be able to access the API or the Database

## 2 - Extended versioning

You can extend the version number by using a hyphen (`-`) and dot (`.`)separated identifiers, where all identifiers must be ASCII only. For example:

- MAJOR.MINOR.PATCH-rc.1
- MAJOR.MINOR.PATCH-alpha.2
- MAJOR.MINOR.PATCH-beta.3

## 3 - Build metadata

Build metadata can be included with a plus sign (`+`), containing only ASCII. For example:

- MAJOR.MINOR.PATCH+exp.sha.5114f85
- MAJOR.MINOR.PATCH-beta.3+21AF26D3
- MAJOR.MINOR.PATCH+20130313144700

## 4 - Precedence

This is how the versions can be organized when ordered, where each version is compared numerically. For example:

- 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1

When MAJOR, MINOR and PATCH are equal, pre-release takes a lower precedence than a normal version. For example:

- 1.0.0-alpha < 1.0.0

If all of the three and the identifier are equal, then a comparison of each dot will be made from left to right until a difference is found. For example:

- 1.0.0-alpha < 1.0.0-alpha.1 < 1.0.0-beta < 1.0.0-beta.2 < 1.0.0-beta.11 < 1.0.0-rc.1 < 1.0.0
