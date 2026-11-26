# ADOM for Apple Silicon

A native build of **ADOM (Ancient Domains of Mystery) 3.3.3** for Macs with Apple Silicon (M1 or later). No emulator, Wine, VM or Rosetta needed.

ADOM is © Thomas Biskup, and this build is distributed with his permission. This repository contains only the compiled app, with no source code.

## Download

1. Open the [**Releases**](../../releases/latest) page.
2. Download **ADOM-3.3.3-arm64.zip**.
3. Double-click the zip, then drag **ADOM.app** to your Applications folder.

Requires macOS 11 or later on an Apple Silicon Mac.

## First launch

The app isn't notarized by Apple, so macOS blocks it the first time:

- **Right-click ADOM.app, choose Open, then click Open** in the dialog. You only need to do this once.
- If macOS says the app is "damaged", run this once in Terminal, then open it again:

      xattr -dr com.apple.quarantine /Applications/ADOM.app

ADOM opens in one window of the terminal app you used most recently (Terminal, iTerm2, Ghostty, WezTerm, kitty, Alacritty or Warp). To pick one yourself, run `defaults write local.adom.native terminal iTerm` (or `Terminal`, or another app's name).

## Notes

- The game window is a centred 80×25 area, so the terminal must be at least that size.
- Saves and settings are kept in `~/.adom.data`, as on Linux.
- Esc closes menus and prompts. Alt+key shortcuts still work.
- To check your download: `shasum -a 256 ADOM-3.3.3-arm64.zip` should match `ADOM-3.3.3-arm64.zip.sha256` on the release page.
