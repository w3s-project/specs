# w3up Specifications

> This repository contains the specs for the w3up Protocol and associated subsystems.

## Understanding the meaning of the spec badges and their life cycle

We use the following label system to identify the state of each spec:

- ![wip](https://img.shields.io/badge/status-wip-orange.svg?style=flat-square) - A work-in-progress, possibly to describe an idea before actually committing to a full draft of the spec.
- ![draft](https://img.shields.io/badge/status-draft-yellow.svg?style=flat-square) - A draft that is ready to review. It should be implementable.
- ![reliable](https://img.shields.io/badge/status-reliable-green.svg?style=flat-square) - A spec that has been adopted (implemented) and can be used as a reference point to learn how the system works.
- ![stable](https://img.shields.io/badge/status-stable-brightgreen.svg?style=flat-square) - We consider this spec to close to final, it might be improved but the system it specifies should not change fundamentally.
- ![permanent](https://img.shields.io/badge/status-permanent-blue.svg?style=flat-square) - This spec will not change.
- ![deprecated](https://img.shields.io/badge/status-deprecated-red.svg?style=flat-square) - This spec is no longer in use.

Nothing in this spec repository is `permanent` or even `stable` yet. Most of the subsystems are still a `draft` or in `reliable` state.

## Linting

The CI runs [markdownlint](https://github.com/DavidAnson/markdownlint) via [markdownlint-cli2-action](https://github.com/marketplace/actions/markdownlint-cli2-action) with the rules in [.markdownlint.jsonc](.markdownlint.jsonc).

To run the linter locally you can use [markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2) with `npx markdownlint-cli2 '*.md'` or install [vscode-markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) in vscode.

Optionally [prettier-vscode](https://github.com/prettier/prettier-vscode) can also be use to format code blocks inside markdown files.

## Spellcheck

The CI runs a spellcheck using [md-spellcheck-action](https://github.com/matheus23/md-spellcheck-action).

If you want to use a word that's being flagged by the spellchecker, add it to [.github/workflows/words-to-ignore.txt](./.github/workflows/words-to-ignore.txt).

Since the spellchecker depends on GitHub Actions, the best way to run it locally is with [act](https://github.com/nektos/act), a Docker-based GitHub Actions workflow runner.

When you first run `act`, it will ask what base image to use as a default. The actions in this repo run fine with the default "medium" base image.

Once `act` is installed, you can run the full CI suite with `act pull_request`. This will also run the markdown linting action described above.

## Contribute

[![contribute](https://cdn.rawgit.com/jbenet/contribute-ipfs-gif/master/img/contribute.gif)](https://github.com/ipfs/community/blob/master/CONTRIBUTING.md)

Suggestions, contributions, criticisms are welcome. Though please make sure to familiarize yourself deeply with IPFS, the models it adopts, and the principles it follows.
This repository falls under the IPFS [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md).
