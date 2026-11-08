# motionmaxxing

A raw talking-head take in, a finished short-form video out, on your own Claude plan.

This repository holds the release notes only. The source is private, and so is the package: it comes from
motionmaxxing.thatdevguy.in, for an invite code. Ask for one at https://motionmaxxing.thatdevguy.in.

## Install

You need a Mac with Apple silicon, a Claude plan that includes Claude Code (Pro or Max) and an invite code. The
studio's Claude runs on your own login, never an API key.

Paste the line from your invite email into Terminal (your code is already in it):

```bash
curl -fsSL https://motionmaxxing.thatdevguy.in/install | bash -s MM-XXXX-XXXX-XXXX
mm login    # once: sign in to Claude
mm          # opens the studio at http://localhost:5199: create your account with your email and the same code
```

The line checks your code first, installs [Homebrew](https://brew.sh) if your Mac hasn't got it, then
`brew install subh05sus/tap/motionmaxxing`. Read what it does first: open
https://motionmaxxing.thatdevguy.in/install in a browser.

The first time, the studio opens on its setup page: **Set up everything** installs the editing tools, the
transcription model and the renderer (3.3 GB, once). `mm doctor` lists what is still missing, `mm app` puts
motionmaxxing.app in ~/Applications for the Dock.

## Update

The studio shows an update card when a new version is out: one click updates and restarts it. Or in Terminal:

```bash
mm update
```

Updates need no code: once you are signed in, the studio keeps a key of this Mac's own for them.

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
