# Monobase

![Tests](https://github.com/cha0sg0d/monorepo/actions/workflows/test.yml/badge.svg)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repo will provide an unopinionated, forakable template for making monorepo projects.

For those interested, this README will document the rationale behind each of the tools used.

## Npm workspaces

1. Create a `workspaces` field in [package.json](./package.json)

## Prettier

1. Install prettier at the top level: `npm i -D prettier`
2. Create a prettier config file: `echo {}> .prettierrc.json`
3. Integrate with editor. For VSCode, make sure `format on save` is true and Prettier is the default formatter (https://github.com/prettier/prettier-vscode#default-formatter)

## Eslint

For Javascript code review

In other words, use Prettier for formatting and linters for catching bugs!

## Husky + Commitlint

https://prettier.io/docs/en/install.html#git-hooks

## Conventional Commits

`npx husky add .husky/commit-msg  'npx --no -- commitlint --edit ${1}'`

## VSCode Settings

## Github Actions (w badge)

## Sample Typescript package
