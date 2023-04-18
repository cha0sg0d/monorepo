# Monobase

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repo will provide an unopinionated, forakable template for making monorepo projects.

For those interested, this README will document the rationale behind each of the tools used and how to set them up.

The finished product is as follows:

- [x] Eslint for code formatting
- [x] Prettier for code styling
- [x] Run prettier + eslint automatically on each commit
- [x] Enforce [conventional commit](https://github.com/conventional-changelog/commitlint) messages
- [x] Github Action to Lint + Format on each push (and tests once we have them)
- [x] Recommended VS Code settings
- [x] npm workspaces

## Npm workspaces

To learn more about monorepos and npm workspaces, check out this [article](https://ruanmartinelli.com/posts/npm-7-workspaces-1)

1. Create a `workspaces` field in [package.json](./package.json)

## Prettier

A tool for standardizing the format of your code.

1. Install prettier at the top level: `npm i -D prettier`
2. Create a prettier config file: `echo {}> .prettierrc.json`
3. Integrate with editor. For VSCode, make sure `format on save` is true and Prettier is the default formatter (https://github.com/prettier/prettier-vscode#default-formatter)

## Eslint

For Javascript code review.

Follow steps [here](https://eslint.org/docs/latest/use/getting-started#manual-set-up).

Use Prettier for formatting and linters for catching bugs!

## Husky + Commitlint

Follow [these steps](https://prettier.io/docs/en/install.html#git-hooks) to set up an action that runs before every commit you make.

## Conventional Commits

Assumes you set up Husky in the previous step. This enforces that your commits follow the conventional commit [spec](https://www.conventionalcommits.org/en/v1.0.0/#examples)

1. `npx husky add .husky/commit-msg  'npx --no -- commitlint --edit ${1}'`

## VSCode Settings

Check out the [.vscode](./vscode) folder for recommended extensions.

## Github Action

To run some checks, like linting and tests on every push to Github, check out this [file](./github/test.yml)

Fun fact: You can display the results of your checks here ![Tests](https://github.com/cha0sg0d/monorepo/actions/workflows/test.yml/badge.svg)

## Sample Typescript package

TODO
