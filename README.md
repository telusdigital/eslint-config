# ESLint Config

## Notice

This package is no longer maintained. Please use [telus-standard] (https://github.com/telus/telus-standard) with TELUS specific linting and a11y rules.

[![version][npm-image]][npm-url] [![Build Status][circle-image]][circle-url]

> TELUS Flavour ESLint [config][shared-config].  
> We inherit from the excellent [Airbnb ESLint config][eslint-config-airbnb] and introduce some more strict requirements.

## Usage

#### 1. add to `.eslintrc`

```json
{
  "extends": "@telus/eslint-config"
}
```

#### 2. install

```bash
npm install eslint @telus/eslint-config
npx install-group peer --package @telus/eslint-config --no-save
```

#### 3. run!

##### cli

```bash
npx eslint .
```

##### git hooks

```bash
echo -e '#!/bin/bash\nnpx eslint .' > .git/hooks/pre-commit && chmod +x .git/hooks/pre-commit
```

##### editors

editors with built-in `eslint` features, _(e.g. [Visual Studio Code][vs-code])_ usually depend on globally installed packages 

---
> Github: [@telus](https://github.com/telus) &bull; 
> Twitter: [@telusdigital](https://twitter.com/telusdigital)

[circle-url]: https://circleci.com/gh/telus/eslint-config
[circle-image]: https://img.shields.io/circleci/project/github/telus/eslint-config/master.svg?style=for-the-badge&logo=circleci

[npm-url]: https://www.npmjs.com/package/@telus/eslint-config
[npm-image]: https://img.shields.io/npm/v/@telus/eslint-config.svg?style=for-the-badge&logo=npm

[eslint-config-airbnb]: https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb
[shared-config]: https://eslint.org/docs/developer-guide/shareable-configs
[vs-code]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
