# 2SR prettier

## Usage

Installing the package will make a symlink in the root of your project to the
prettier config in this repo. It is recommended to add `.prettierrc` to your
`.gitignore` so you don't accidentally commit the symlink.

```bash
npm install @twostoryrobot/prettier
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
