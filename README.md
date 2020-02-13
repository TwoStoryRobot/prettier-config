[![npm (scoped)](https://img.shields.io/npm/v/@twostoryrobot/prettier-config.svg)](https://www.npmjs.com/package/@twostoryrobot/prettier-config)


# 2SR prettier

Get pretty code with prettier the way Two Story Robot likes it.

## Usage

```bash
npm install --save-dev @twostoryrobot/prettier-config
```

Then you can source the config from your own `.prettierrc.js`.

```js
module.exports = require('@twostoryrobot/prettier-config')
```

Or if you want to override the default at all (Note: please consider making a PR
if you think the override will be useful for other projects).

```js
const prettierConfig = require('@twostoryrobot/prettier-config')
module.exports = Object.assign({}, prettierConfig, { semi: true })
```

Make sure to install the peer dependencies

```bash
npx install-peerdeps --dev @twostoryrobot/prettier-config
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
 "husky": {
    "hooks": {
      "pre-commit": "prettier --list-different '**/*.js'"
    }
  }
}
```
