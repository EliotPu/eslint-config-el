# JavaScript EL Style - ESLint Shareable Config

[![CI](https://github.com/standard/eslint-config-standard/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/standard/eslint-config-standard/actions/workflows/ci.yml)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)

This config extends and overites some of the [`ESlint:recommended`](https://eslint.org/) & [`Standard`](https://standardjs.com) via [`eslint-config-standard`](https://www.npmjs.com/package/eslint-config-standard?activeTab=readme).

ESM style.

## Install

```bash
npm install --save-dev eslint-config-el
```

The project needs some packages for the extend ESLint config:

* "eslint-plugin-promise"
* "eslint-plugin-import"
* "eslint-plugin-n"

```bash
npm install --save-dev eslint-plugin-promise eslint-plugin-import eslint-plugin-n
```

**Whole together**, run the following command:

```bash
npm install --save-dev eslint-config-el eslint-plugin-promise eslint-plugin-import eslint-plugin-n
```

## Usage

Shareable configs are designed to work with the `extends` feature of `.eslintrc` files.
You can learn more about
[`Shareable Configs`](http://eslint.org/docs/developer-guide/shareable-configs) on the
official ESLint website.

Then, add this to your `.eslintrc` file:

```json
{
  "extends": "el"
}
```

or

```json
{
  "root": true,
  "extends": "el"
}
```

**"root": true**

> To limit ESLint to a specific project, place "root": true inside the .eslintrc.* file or eslintConfig field of the package.json file or in the .eslintrc.* file at your project's root level. ESLint stops looking in parent folders once it finds a configuration with "root": true .

[Cascading and hierarchy in Configuration Files](https://eslint.org/docs/latest/use/configure/configuration-files#cascading-and-hierarchy).

**Important!**

ESLint config's field "env": seted only "es2022" in true.
And `"es2021": true`, `"node": true` in [eslint-config-standard](https://github.com/standard/eslint-config-standard/blob/master/.eslintrc.json).
In your project set your environments. All environment options [`see`](https://eslint.org/docs/latest/use/configure/language-options#specifying-environments).

*Example:*

```json
{
  "root": true,
  "env": {
    "browser": true,
    "node": false,
    "mocha": true
    ...
  },
  "extends": "el"
}
```

*Note: We omitted the `eslint-config-` prefix since it is automatically assumed by ESLint.*

*Note: You may want your IDE to highlight the code according to the rules of the config,
and if you are the owner of the VS Code,
you will need an [`ESLint plugin`](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) for it.
**You may need just wait a bit or to restart the IDE.***

You can override settings from the shareable config by adding them directly into your
`.eslintrc` file. All rules [`see`](https://eslint.org/docs/latest/rules/).

*Example:*

```json
{
  "root": true,
  "extends": "el",
  "rules": {
    "indent": [
      "error",
      4,
      {
        "SwitchCase": 0
      }
    ],
    ...
  }
}
```

In addition to fixes in the IDE itself (if you have the ESLint extension),
you can use the command line by writing `npx eslint .` - to show admonitions and `npx eslint . --fix` - to fix it.
You can also add scripts to your package, for example:

*NOTE: ("`.`" - points to the project root, check everything in starting from the project root)*

### Looking for something easier than this?

The easiest way to use JavaScript Standard Style to check your code is to use the
[`standard`](http://standardjs.com) package. This comes with a global
Node command line program (`standard`) that you can run or add to your `npm test` script
to quickly check your style.

Or another style something like this [`ESLint`](https://eslint.org/docs/latest/use/getting-started).

## Author

**EliotPu <78807845+EliotPu@users.noreply.github.com>**

* [<img alt="GitHub" width="18px" src="https://raw.githubusercontent.com/EliotPu/ESLint-config-El/main/tech/github-logo.png" /> GitHub](https://github.com/EliotPu)
