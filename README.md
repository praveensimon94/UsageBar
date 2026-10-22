# UsageBar

AI usage and reset times in your Mac’s menu bar.

Connect **Codex, Cursor, Claude Code, Antigravity, and GitHub Copilot**. Every connected tool gets its own menu bar logo and usage percentage. Pinning keeps a tool first in the scrollable overview and Connections list.

## Download

Download the DMG from [Releases](https://github.com/praveensimon94/UsageBar/releases). Requires **macOS 14 or later**, on Apple Silicon or Intel.

1. Open the DMG and drag **UsageBar.app** to **Applications**.
2. Open UsageBar. Its icon appears in the menu bar.
3. Open **Settings → Connections** and connect your tools.

This independent build is ad-hoc signed, without Apple notarization. If macOS blocks the first launch, try opening the app, then open **System Settings → Privacy & Security → Open Anyway** for UsageBar. Approve only downloads from a source you trust. You do not need to disable your Mac’s security protections.

## Connections

- **Codex:** sign in to Codex on your Mac.
- **Cursor:** sign in to the Cursor desktop app.
- **Claude:** run `claude auth login`; allow UsageBar to read Claude Code’s Keychain item when connecting if macOS asks.
- **Antigravity:** sign in and keep the Antigravity app running.
- **GitHub Copilot:** use `gh auth login`, or supply a GitHub token in UsageBar’s connection settings.

UsageBar reads existing local credentials and sends usage requests directly to the relevant provider. Manually supplied tokens are stored in your Mac’s Keychain. Disconnect stops polling and clears UsageBar’s saved access and cached usage. It preserves your sign-in in the original tool.

Some usage endpoints are undocumented and can change. Missing usage is shown as unavailable, rather than a zero reading. Gemini chat/CLI is not included.

## Updates

Open **Settings → Updates** to check for updates or enable automatic checks. Updates are verified using Sparkle’s Ed25519 signatures, independently of Apple’s developer program. The first public release must be published before the update channel becomes available.

Release downloads include `SHA256SUMS` for manual verification. This repository hosts release assets and instructions; application source is maintained separately.

## Open-source acknowledgements

UsageBar bundles [CodexBar’s usage collectors](https://github.com/steipete/CodexBar) and [Sparkle](https://sparkle-project.org/). Full licenses and dependency notices are included in the app under **Settings → About → Open source licenses**.
