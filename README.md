# 2SR prettier

## Usage

```bash
npm install --save-dev @twostoryrobot/prettier
```

Then you can source the config from your own `prettier.config.js`.

```js
module.exports = require('@twostoryrobot/prettier')
```

Or if you want to override the default at all.

```js
const prettierConfig = require('@twostoryrobot/prettier')
module.exports = Object.assign({}, prettierConfig, { semi: true })
```

Make sure to install the peer dependencies

```bash
npm install --save-dev prettier
```

### Scripts

Now you can add a script to your project's package.json that calls prettier and
it will reference the config file in the root of your project directory.

```json
"scripts": {
  "prettier": "prettier --write '**/*.js'"
}
```

### Hooks

If you install [husky](https://github.com/typicode/husky) you can invoke
prettier as a hook for various actions (precommit, prepush, etc)

```json
"scripts": {
  "precommit": "prettier --write '**/*.js'"
}
```
