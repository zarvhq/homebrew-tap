# zarvhq Homebrew Tap

[Homebrew](https://brew.sh) formulae for zarvhq's internal tools. Public tap,
prebuilt binaries — `brew install` needs no GitHub token.

## How do I install these formulae?

```sh
brew install zarvhq/tap/<formula>
```

Or tap first, then install by name:

```sh
brew tap zarvhq/tap
brew install <formula>
```

Or add it to a [`Brewfile`](https://docs.brew.sh/Brew-Bundle-and-Brewfile):

```ruby
tap "zarvhq/tap"
brew "repo-monitor"
```

## Available formulae

| Formula | Description | Install |
|---|---|---|
| [**repo-monitor**](https://github.com/zarvhq/repo-monitor) | Monitor open PRs and active CIs for a GitHub org/user from the terminal (Bubble Tea TUI) | `brew install zarvhq/tap/repo-monitor` |

## Updating

```sh
brew update
brew upgrade <formula>          # a single tool
brew upgrade                    # everything, including this tap
```

## Notes

- **Cross-platform:** formulae ship prebuilt binaries for macOS and Linux
  (Intel + Apple Silicon / arm64).
- **Public on purpose:** the tap is public so installs work without
  authentication, even though some source repos are private.
- **Auth at runtime:** the tools themselves use your existing
  [`gh`](https://cli.github.com) credentials (or `GH_TOKEN` / `GITHUB_TOKEN`) to
  talk to the GitHub API.

## How releases land here

Formulae and their binaries are published automatically by
[GoReleaser](https://goreleaser.com) when a tool is tagged — it builds the
binaries, attaches them to a GitHub Release in this repo, and commits the
generated formula to [`Formula/`](Formula). Formula files are generated; **don't
edit them by hand**.

## Documentation

For general Homebrew usage: `brew help`, `man brew`, or the
[Homebrew documentation](https://docs.brew.sh).
