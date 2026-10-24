# motionmaxxing

A raw talking-head take in, a finished short-form video out, on your own Claude plan.

This repository holds the releases only: the built package for macOS on Apple silicon. The source is private.

## Install

You need a Mac with Apple silicon, [Homebrew](https://brew.sh) and a Claude plan that includes Claude Code (Pro or
Max). The studio's Claude runs on your own login, never an API key.

```bash
brew tap subh05sus/tap
brew install motionmaxxing
mm login    # once: sign in to Claude
mm          # opens the studio at http://localhost:5199
```

The first time, the studio opens on its setup page: **Set up everything** installs the editing tools, the
transcription model and the renderer (3.3 GB, once). `mm doctor` lists what is still missing, `mm app` puts
motionmaxxing.app in ~/Applications for the Dock.

## Update

The studio shows an update card when a new version is out: one click updates and restarts it. Or in Terminal:

```bash
brew upgrade motionmaxxing && mm stop && mm
```

## Uninstall

```bash
mm stop
brew uninstall motionmaxxing
brew untap subh05sus/tap                 # optional
rm -rf ~/Applications/motionmaxxing.app  # optional: the Dock app
```

Two folders stay until you delete them yourself: `~/Movies/motionmaxxing` (your videos and library) and
`~/.motionmaxxing` (the editing tools and models, about 3.3 GB, and what the studio learned of your taste).

## Licence

motionmaxxing is proprietary software: see `LICENSE` in the package. Versions up to 0.12.x were released under the
MIT License and stay under it. The code of others it includes keeps its own licences (`THIRD_PARTY_NOTICES.md` and
`THIRD_PARTY_LICENSES.txt` in the package).

## Problems and ideas

Open an [issue](../../issues).
