# EsLint


## Install eslint in project

### React
install this libs

```shell
yarn add eslint -D
// or
npm install eslint --save-dev
```

### Init eslint setup
```shell
npx eslint --init
```

> When running this command, you will need to answer some questions about the configuration


### Libs
Libs used in React Typescript project

```json
  "@typescript-eslint/eslint-plugin"
  "@typescript-eslint/parser"
  "eslint-config-airbnb"
  "eslint-import-resolver-babel-plugin-root-import"
  "eslint-plugin-import"
  "eslint-plugin-jest"
  "eslint-plugin-jsx-a11y"
  "eslint-plugin-react"
  "eslint-plugin-react-hooks"
```

### Add Rules
Rules used in Decathlon project

```js
rules: {
  'no-console': [ 1, { allow: [ 'warn', 'error' ] }],
  'comma-dangle': [ 'error', 'always-multiline' ],
  'no-use-before-define': 'off',
  indent: [ 'error', 2, { SwitchCase: 1 }],
  'no-empty-function': 'error',
  'prefer-const': 'error',
  'no-plusplus': [ 'error', { allowForLoopAfterthoughts: true }],
  'newline-before-return': 'error',
  'max-len': [ 'error', { code: 120, ignorePattern: '^import\\W.*' }],
  'no-multiple-empty-lines': [ 'error', { max: 1, maxBOF: 0, maxEOF: 0 }],
  'eol-last': [ 'error', 'always' ],
  'import/prefer-default-export': 0,
  'import/no-extraneous-dependencies': 0,
  'import/no-cycle': [ 2, { maxDepth: 1 }],
  'import/no-named-as-default': 0,
  'import/no-named-as-default-member': 0,
  'import/extensions': 'off',
  'import/order': 0,
  'import/no-unresolved': 'off',
  semi: [ 'error', 'never' ],
  'object-curly-spacing': [ 'error', 'always' ],
  'object-curly-newline': [ 'error', {
    multiline: true,
    consistent: true,
    minProperties: 4,
  }],
  'array-bracket-spacing': [ 'error', 'always', {
    objectsInArrays: false,
    arraysInArrays: false,
  }],
},
```

## React Project
Rules used in React project

```js
'react/prefer-stateless-function': 0,
'react/prop-types': 0,
'react/require-default-props': 0,
'react/jsx-filename-extension': 0,
'react/jsx-one-expression-per-line': 0,
'react/jsx-props-no-spreading': 0,
'react/button-has-type': 0,
```

## Typescript Project
Rules used in React with Typescript project

```js
'@typescript-eslint/no-use-before-define': 'error',
'@typescript-eslint/no-explicit-any': 0,
'@typescript-eslint/explicit-module-boundary-types': 'off',
'@typescript-eslint/no-empty-function': [
  'error',
  { allow: [ 'arrowFunctions' ] },
],
'@typescript-eslint/indent': [ 'warn', 2 ],
'@typescript-eslint/no-var-requires': 'off',
```

## Refs
[How to install Eslint](https://andrebnassis.medium.com/setting-eslint-on-a-react-typescript-project-2021-1190a43ffba)
