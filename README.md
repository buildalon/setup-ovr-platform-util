# Buildalon Setup ovr-platform-util

[![Discord](https://img.shields.io/discord/939721153688264824.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/VM9cWJ9rjH) [![marketplace](https://img.shields.io/static/v1?label=&labelColor=505050&message=Buildalon%20Actions&color=FF1E6F&logo=github-actions&logoColor=0076D6)](https://github.com/marketplace?query=buildalon) [![validate](https://github.com/buildalon/setup-ovr-platform-util/actions/workflows/validate.yml/badge.svg?branch=main&event=push)](https://github.com/buildalon/setup-ovr-platform-util/actions/workflows/validate.yml)

A GitHub Action to setup the [`ovr-platform-utility`](https://developer.oculus.com/resources/publish-reference-platform-command-line-utility) tool command alias.

## How to use

```yaml
jobs:
  validate:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os: [ macos-latest, windows-latest, macos, windows ]
    steps:
        # download and setup ovr platform util
      - uses: buildalon/setup-ovr-platform-util@v1
        # run commands
      - run: 'ovr-platform-util version'
```
