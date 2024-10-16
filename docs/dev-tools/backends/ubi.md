# Ubi Backend <Badge type="warning" text="experimental" />

You may install GitHub Releases and URL packages directly using [ubi](https://github.com/houseabsolute/ubi) backend.

The code for this is inside of the mise repository at [`./src/backend/ubi.rs`](https://github.com/jdx/mise/blob/main/src/backend/ubi.rs).

## Usage

The following installs the latest version of goreleaser
and sets it as the active version on PATH:

```sh
$ mise use -g ubi:goreleaser/goreleaser
$ goreleaser --version
1.25.1
```

The version will be set in `~/.config/mise/config.toml` with the following format:

```toml
[tools]
"ubi:goreleaser/goreleaser" = "latest"
```

### Supported Ubi Syntax

| Description                                   | Usage                                                                                                   |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| GitHub shorthand for latest release version   | `ubi:goreleaser/goreleaser`                                                                             |
| GitHub shorthand for specific release version | `ubi:goreleaser/goreleaser@1.25.1`                                                                      |
| URL syntax                                    | `ubi:https://github.com/goreleaser/goreleaser/releases/download/v1.16.2/goreleaser_Darwin_arm64.tar.gz` |

Other syntax may work but is unsupported and untested.
