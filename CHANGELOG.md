# Change Log

El project adheres to [Semantic Versioning](http://semver.org/).

* ESLint
[Website](https://eslint.org)

* Standard
[Website](https://standardjs.com/).

  All notable changes to Standard project will be documented in the
[`standard` CHANGELOG](https://github.com/standard/standard/blob/master/CHANGELOG.md).

  Standard project's
[commit log](https://github.com/standard/eslint-config-standard/commits/master) is
also quite readable.


## [1.1.0] - 2023-07-10

### Added
- [package] [`engines`]: add supported engine and package manager
  * `node`: `>=16.13.1`,
  * `npm`: `>=7.10.0`

### Changed
- [readme]: remove some packages installation and change structure
  * removed the installation block packages
  ("eslint-plugin-promise", "eslint-plugin-import", "eslint-plugin-n"). Because, they pull up
  * redesigned file structure: notes are moved below information block of usage section
  * Add a mention to the readme file with a link to specify parser options
  * rewritten some text
- [`env`] [`es2024`]: change ECMA `es2022` -> `es2024`
- [`complexity`]: change `complexity` from `2` to `10`
- [`quotes`]: changed `quotes`. Add `avoidEscape` and `allowTemplateLiterals` (true value)
- [`no-inline-comments`]: disable `no-inline-comments`
- [`newline-per-chained-call`]: change `ignoreChainWithDepth` from `1` to `2`
- [`newline-per-chained-call`]: supplements `lines-around-comment`. Allow comments at the beginning of objects, arrays, classes.
`applyDefaultIgnorePatterns` and `afterHashbangComment` is `true`
