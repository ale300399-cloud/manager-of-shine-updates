# MANAGER OF SHINE macOS updater channel

This is a **separate channel** from the Android Capgo updater. Do not overwrite Android update files.

## Public static endpoint
After release approval, publish `macos/latest.json` here. Tauri's HTTPS feed URL can be:
`https://raw.githubusercontent.com/ale300399-cloud/manager-of-shine-updates/main/macos/latest.json`

The JSON must be generated from an actual signed Apple Silicon `.app.tar.gz` with its matching Tauri `.sig` using `scripts/create-macos-ota-feed.mjs` in the private app repository. The `url` in the JSON must point to a publicly downloadable HTTPS archive (for example a public GitHub Release asset); do not use private Actions artifacts or GitHub blob links.

**Status: not active.** No `latest.json` is published until signed archives, key pinning, and an actual update test are ready. Never publish signing private keys, passwords, or customer data here. Keep Android and macOS packages isolated.
