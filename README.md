# Buildalon Setup ovr-platform-util

[![Discord](https://img.shields.io/discord/939721153688264824.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/VM9cWJ9rjH) [![marketplace](https://img.shields.io/static/v1?label=&labelColor=505050&message=Buildalon%20Actions&color=FF1E6F&logo=github-actions&logoColor=0076D6)](https://github.com/marketplace?query=buildalon) [![validate](https://github.com/buildalon/setup-ovr-platform-util/actions/workflows/validate.yml/badge.svg?branch=main&event=push)](https://github.com/buildalon/setup-ovr-platform-util/actions/workflows/validate.yml)

A GitHub Action to setup the [`ovr-platform-util`](https://developers.meta.com/horizon/resources/publish-reference-platform-command-line-utility/) tool command alias.

## How to use

```yaml
jobs:
  validate:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os: [ubuntu-latest, macos-latest, windows-latest]
    steps:
        # download and setup ovr platform util
      - uses: buildalon/setup-ovr-platform-util@v2
        # run commands
      - run: 'ovr-platform-util version'
```

### inputs

| Name | Description | Required |
| ---- | ----------- | -------- |
| `self-update` | Automatically update the ovr-platform-util tool when it is restored from the runner tool cache. A fresh download is already the latest version. Defaults to `true`. | false |

### outputs

- `path`: The full path to the ovr-platform-util executable.
- `version`: The installed ovr-platform-util version.

### environment variables

- `OVR_PLATFORM_UTIL_PATH`: The full path to the ovr-platform-util executable.

## Related actions

- [upload-meta-quest-build](https://github.com/buildalon/upload-meta-quest-build)

