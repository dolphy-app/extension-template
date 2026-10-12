<p align="center">
  <img src=".github/logo.svg" width="72" alt="Dolphy logo">
</p>

<h1 align="center">Dolphy extension template</h1>

<p align="center">
  <b>Your first Dolphy extension in minutes.</b><br>
  A ready-to-run workspace with Vue and React examples, tests and live reload.
</p>

<p align="center">
  <a href="https://github.com/dolphy-app/extension-template/actions/workflows/ci.yml"><img src="https://github.com/dolphy-app/extension-template/actions/workflows/ci.yml/badge.svg?branch=main" alt="CI status"></a>
</p>

<p align="center">
  <a href="https://github.com/dolphy-app/extension-template/generate">Use this template</a> ·
  <a href="DEVELOPMENT.md">Development guide</a> ·
  <a href="https://github.com/dolphy-app/extensions">Catalog</a> ·
  <a href="https://github.com/dolphy-app/dolphy">Dolphy app</a>
</p>

Extensions add themes, exercise types, commands, panels and more to [Dolphy](https://github.com/dolphy-app/dolphy). This repository is a pnpm workspace whose layout repeats that of the [extension catalog](https://github.com/dolphy-app/extensions), so every folder in `extensions/` can go into a catalog pull request as it is.

## Start

Click **Use this template → Create a new repository**, clone it and run:

```sh
pnpm install
pnpm test
pnpm dev hello-vue   # starts a watch build and the installed Dolphy app; edits apply live
```

You need Node.js 22.12 or newer, pnpm, and the Dolphy app (0.5.0 or newer) for `pnpm dev`. The tests and the build don't need the app.

## Examples

| Folder                                  | What it shows                                                                                                   |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| [`hello-vue`](extensions/hello-vue)     | A Vue interface: palette commands, a panel and a card in "Today's plan", all written as single-file components. |
| [`hello-react`](extensions/hello-react) | The same drawn with React, plus a card that calls the server part with `useRpc` and the window with `useApp`.   |

Keep what you need, delete the rest, and add your own:

```sh
pnpm create:extension my-extension --template react-panel
```

Templates: `command-panel`, `react-panel`, `exercise`, `events`, `theme`, `blank`.

## Then

Build and test your extension, check it against the catalog rules with `pnpm check`, and publish it with a pull request to [dolphy-app/extensions](https://github.com/dolphy-app/extensions). Commands, lockfiles, publishing steps and limitations are in the [development guide](DEVELOPMENT.md).
