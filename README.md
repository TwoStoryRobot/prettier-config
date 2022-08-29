[![npm (scoped)](https://img.shields.io/npm/v/@twostoryrobot/prettier-config.svg)](https://www.npmjs.com/package/@twostoryrobot/prettier-config)

# TSR prettier

Get pretty code with prettier the way Two Story Robot likes it.

## Usage

```bash
npm install --save-dev @twostoryrobot/prettier-config
```

Then you can source the config from your own `.prettierrc.js`.

```js
module.exports = require('@twostoryrobot/prettier-config')
```

Now you can add a script to your project's package.json that calls prettier and
it will reference the config file in the root of your project directory.

```json
"scripts": {
  "prettier": "prettier --write 'src/**/*.js'",
  "prettier-check": "prettier --list-different 'src/**/*.js'"
}
```

## Custom configuration

If you want to override the defaults at all, use this method:

```js
const prettierConfig = require('@twostoryrobot/prettier-config')
module.exports = Object.assign({}, prettierConfig, { semi: true })
```

_Note: please consider making a PR if you think the override will be useful for
other projects._
