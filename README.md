# tslint-plugin-prettier

[![npm](https://img.shields.io/npm/v/tslint-plugin-prettier.svg)](https://www.npmjs.com/package/tslint-plugin-prettier)
[![build](https://img.shields.io/travis/ikatyang/tslint-plugin-prettier/master.svg)](https://travis-ci.org/ikatyang/tslint-plugin-prettier/builds)
[![coverage](https://img.shields.io/codecov/c/github/ikatyang/tslint-plugin-prettier/master.svg)](https://codecov.io/gh/ikatyang/tslint-plugin-prettier)
[![dependencies](https://img.shields.io/david/ikatyang/tslint-plugin-prettier.svg)](https://david-dm.org/ikatyang/tslint-plugin-prettier)
[![devDependencies](https://img.shields.io/david/dev/ikatyang/tslint-plugin-prettier.svg)](https://david-dm.org/ikatyang/tslint-plugin-prettier?type=dev)

tslint plugin for prettier formatting

**NOTE**: This project uses official reporter from [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier).

[Changelog](https://github.com/ikatyang/tslint-plugin-prettier/blob/master/CHANGELOG.md)

## Sample

```ts
a();;;
//  ~~
;;;
//~ [Delete `;;⏎;;;`]
```

```ts
var foo = ''
//        ~~ [Replace `''` with `"";⏎`]
```

```ts
var foo= "";
//     ~ [Insert `·`]
```

## Install

```sh
# using npm
npm install --save-dev tslint-plugin-prettier prettier

# using yarn
yarn add --dev tslint-plugin-prettier prettier
```

## Usage

(tslint.json)

for `tslint@5.0.0+`

```json
{
  "extends": ["tslint-plugin-prettier"],
  "rules": {
    "prettier": true
  }
}
```

for `tslint@5.2.0+`

```json
{
  "rulesDirectory": ["tslint-plugin-prettier"],
  "rules": {
    "prettier": true
  }
}
```

**NOTE**: To use this plugin, it'd better to also use [tslint-config-prettier-ext](https://github.com/ikatyang/tslint-config-prettier-ext) to disable all prettier-related rules, so as to avoid conflicts between existed rules.

## Options

Same as [Prettier Options](https://github.com/prettier/prettier#options), for example:

```json
{
  "extends": ["tslint-plugin-prettier"],
  "rules": {
    "prettier": [true, { "singleQuote": true }]
  }
}
```

## Development

```sh
# lint
yarn run lint

# build
yarn run build

# test
yarn run test
```

## Related

- [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier)
- [tslint-config-prettier-ext](https://github.com/ikatyang/tslint-config-prettier-ext)

## License

MIT © [Ika](https://github.com/ikatyang)
