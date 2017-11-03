# ESLint Config [![version][npm-version]][npm-url] [![License][license-image]][license-url]

> TELUS Flavour ESLint [config][shared-config].

> We inherit from the excellent [Airbnb ESLint config][eslint-config-airbnb] and introduce some more strict requirements.

## Usage

Our default export contains all of our ESLint rules, including ECMAScript 6+ and React. It requires `eslint`, `eslint-plugin-import`, `eslint-plugin-react`, and `eslint-plugin-jsx-a11y`.

If you use yarn, run `yarn add --dev @telusdigital/eslint-config-base eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y`.

If you use Docker for local development, you would have to run the ESLint fix with `yarn` with the command line, through your `package.json`, before you build the container. Your build will break if you try to run ESLint fix through Docker.

1. Install the correct versions of each package, which are listed by the command:

  ```sh
  yarn info "@telusdigital/eslint-config@latest" peerDependencies
  ```

  You can either install all the peer dependencies manually or use the [install-peerdeps][install-peer-deps] cli tool.

  ```sh
  yarn global add install-peerdeps
  install-peerdeps --dev @telusdigital/eslint-config
  ```

  The cli will produce and run a command like:

  ```sh
  yarn install --save-dev @telusdigital/eslint-config eslint@^#.#.# eslint-plugin-jsx-a11y@^#.#.# eslint-plugin-import@^#.#.# eslint-plugin-react@^#.#.#
  ```

2. Add to your `.eslintrc`

```json
{
  "extends": "@telusdigital/eslint-config"
}
```

---
> :copyright: [TELUS digital](https://labs.telus.com/)  · 
> License: [ISC][license-url]  · 
> Github: [@telusdigital](https://github.com/telusdigital)  · 
> Twitter: [@telusdigital](https://twitter.com/telusdigital)

[license-url]: http://choosealicense.com/licenses/isc/
[license-image]: https://img.shields.io/github/license/telusdigital/eslint-config.svg?style=flat-square

[npm-url]: https://www.npmjs.com/package/@telusdigital/eslint-config
[npm-version]: https://img.shields.io/npm/v/@telusdigital/eslint-config.svg?style=flat-square
[npm-downloads]: https://img.shields.io/npm/dm/@telusdigital/eslint-config.svg?style=flat-square

[eslint-config-airbnb]: https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb
[shared-config]: https://eslint.org/docs/developer-guide/shareable-configs
[install-peerdeps]: https://github.com/nathanhleung/install-peerdeps
