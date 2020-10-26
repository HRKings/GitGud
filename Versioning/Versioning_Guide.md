# GitGud: Versioning Submodel

- [GitGud: Versioning Submodel](#gitgud-versioning-submodel)
	- [1 - Version Convention](#1---version-convention)
		- [1.1 - Extended versioning](#11---extended-versioning)
		- [1.2 - Build metadata](#12---build-metadata)
	- [2 - Ordering](#2---ordering)
	- [3 - Range Guidelines](#3---range-guidelines)
		- [3.1 - Basic Range](#31---basic-range)
		- [3.2 - Wildcard Range](#32---wildcard-range)
		- [3.3 - Greater and Less Range](#33---greater-and-less-range)

---

This versioning guide is an expanded version of the [Semantic Versioning](https://semver.org). But if you want to more details about the SemVer, head the website to read more.

## 1 - Version Convention

Basic versioning is done in the form of: `MAJOR.MINOR.PATCH`, where:

- MAJOR version is when you make changes that are incompatible with a previous version;
- MINOR version is when you add functionality in a backwards compatible manner;
- PATCH version is when you make backwards compatible bug fixes.

Where backwards compatible means that a user using a previous version can still use and interact with services provided in the current versions, for example:

- In a game, it will not break saves or corrupt data
- In a software, it will still be able to access the API or the Database

**Obs.:** On this model, some degree of breaking changes are allowed in the *MINOR* and *PATCH* version. This is due some changes not being in control of the developer, for example, external Dependencies changes, if those changes break the code, they can still be considered *MINOR* (changed functionality) or *PATCH* (fix for some third-party change).

### 1.1 - Extended versioning

You can extend the version number by using a hyphen (`-`) and dot (`.`)separated identifiers, where all identifiers must be ASCII only. For example:

- MAJOR.MINOR.PATCH-rc.1
- MAJOR.MINOR.PATCH-alpha.2
- MAJOR.MINOR.PATCH-beta.3

### 1.2 - Build metadata

Build metadata can be included with a plus sign (`+`), containing only ASCII. For example:

- MAJOR.MINOR.PATCH+exp.sha.5114f85
- MAJOR.MINOR.PATCH-beta.3+21AF26D3
- MAJOR.MINOR.PATCH+20130313144700

## 2 - Ordering

This is how the versions can be organized when ordered, where each version is compared numerically. For example:

- 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1

When MAJOR, MINOR and PATCH are equal, pre-release takes a lower precedence than a normal version. For example:

- 1.0.0-alpha < 1.0.0

If all of the three and the identifier are equal, then a comparison of each dot will be made from left to right until a difference is found. For example:

- 1.0.0-alpha < 1.0.0-alpha.1 < 1.0.0-beta < 1.0.0-beta.2 < 1.0.0-beta.11 < 1.0.0-rc.1 < 1.0.0

## 3 - Range Guidelines

When working with dependencies, you will probably need to work with ranges to cover more than one version.

### 3.1 - Basic Range

To work with a basic range of versions, you need to specify the starting version and the ending version with a hyphen (`-`), for example:

`1.0.0 - 2.0.0`, this means that any version between `1.0.0` and `2.0.0` is accepted (including `1.0.0` and `2.0.0`).

### 3.2 - Wildcard Range

You can specify a greater range of versions using the wildcard asterisk (`*`), for example:

- `*.0.0`, will accept any version with the MINOR and PATCH versions equal to 0;
- `1.*.0`, will accept any version with the MAJOR version equal to 1 and the PATCH equal to 0;
- `1.0.*`, will accept any version with the MAJOR version equal to 1 and MINOR equal to 0;
- `1.*.*`, will accept any version with the MAJOR version equal to 1.

### 3.3 - Greater and Less Range

If you need to support a minimum or maximum version you can use the operators grater than (`>`) and lesser then (`<`), for example:

- `>1.0.0`, will accept any version above `1.0.0`;
- `<1.0.0`, will accept any version bellow `1.0.0`.
