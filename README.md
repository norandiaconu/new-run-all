| index | [new-run-all] | [run-s] | [run-p] | [Node API] |
|-------|---------------|---------|---------|------------|

# new-run-all

A CLI tool to run multiple npm-scripts in parallel or sequential. Forked from npm-run-all to update dependencies. https://github.com/mysticatea/npm-run-all

## ⤴️ Motivation

- **Simplify.** The official `npm run-script` command cannot run multiple scripts, so if we want to run multiple scripts, it's redundant a bit. Let's shorten it by glob-like patterns.<br>
  Before: `npm run clean && npm run build:css && npm run build:js && npm run build:html`<br>
  After: `new-run-all clean build:*`
- **Cross platform.** We sometimes use `&` to run multiple command in parallel, but `cmd.exe` (`npm run-script` uses it by default) does not support the `&`. Half of Node.js users are using it on Windows, so the use of `&` might block contributions. `new-run-all --parallel` works well on Windows as well.

## 💿 Installation

```bash
$ npm install new-run-all --save-dev
# or
$ yarn add new-run-all --dev
```

## 📖 Usage

### CLI Commands

This `new-run-all` package provides 3 CLI commands.

- [new-run-all]
- [run-s]
- [run-p]

The main command is [new-run-all].
We can make complex plans with [new-run-all] command.

Both [run-s] and [run-p] are shorthand commands.
[run-s] is for sequential, [run-p] is for parallel.
We can make simple plans with those commands.

#### Yarn Compatibility

If a script is invoked with Yarn, `new-run-all` will correctly use Yarn to execute the plan's child scripts.

### Node API

This `new-run-all` package provides Node API.

- [Node API]

## 📰 Changelog

- https://github.com/norandiaconu/new-run-all/releases

## 🍻 Contributing

Welcome♡

### Bug Reports or Feature Requests

Please use GitHub Issues.

### Correct Documents

Please use GitHub Pull Requests.

I'm not familiar with English, so I especially thank you for documents' corrections.

### Implementing

Please use GitHub Pull Requests.

There are some npm-scripts to help developments.

- **npm test** - Run tests and collect coverage.
- **npm run clean** - Delete temporary files.
- **npm run lint** - Run ESLint.
- **npm run watch** - Run tests (not collect coverage) on every file change.

[new-run-all]: docs/new-run-all.md
[run-s]: docs/run-s.md
[run-p]: docs/run-p.md
[Node API]: docs/node-api.md
