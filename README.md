# deck

**one deck for all your agents**

Deck is a terminal app for running Claude Code, Codex, OpenCode and Antigravity side by side in one chat. It drives the CLIs you already have, under your own logins: a session holds you and any number of agents, they can hand work to each other where you can see it, and every reply, tool call, diff and approval shows up in one place.

Deck never calls a model API and never reads a credential. It sends no telemetry and checks for no updates.

This repository only holds Deck's releases and installers.

## Install

macOS and Linux:

```sh
curl -fsSL https://raw.githubusercontent.com/dev-dami/deck-releases/main/install.sh | sh
```

Windows (PowerShell):

```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/dev-dami/deck-releases/main/install.ps1 | iex"
```

Both install the latest release, checked against its checksum: to `~/.local/bin` on macOS and Linux, and to `%LOCALAPPDATA%\deck\bin` on Windows, which is added to your PATH.

- `DECK_VERSION` picks a release, e.g. `DECK_VERSION=v0.8.0-dev`. Pre-releases are only installed by name.
- `DECK_INSTALL_DIR` installs somewhere else.

Or download an archive from [Releases](https://github.com/dev-dami/deck-releases/releases) and check it against `checksums.txt`.

## Getting started

Deck uses the agent CLIs you have installed and signed in to: `claude`, `codex`, `opencode`, `agy`.

```sh
deck doctor   # which agents Deck found
deck          # start in a project folder
```

## License

Copyright © 2026 dev-dami. All rights reserved. The releases here may be installed and used; third-party notices are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
