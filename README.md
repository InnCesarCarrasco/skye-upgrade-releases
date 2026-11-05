# Skye Upgrade releases

Signed releases of the Skye upgrade assistant: the engine and the rules that find and fix what a Skye upgrade changes in a project's custom SCSS, CSS and JavaScript.

This repository only holds finished releases. The assistant runs on your computer. Your code is never uploaded.

## Use it

1. Download `skye-upgrade-setup.mjs` from the [latest release](../../releases/latest).
2. In the root folder of your Skye project, run: `node skye-upgrade-setup.mjs`
3. Check that the public key fingerprint it prints matches the one below.
4. Commit the new `tools/skye-upgrade/` folder, then run `npm run skye:upgrade:dry -- --from <current> --to <target>`.

Needs Node 18.3 or newer.

## Public key fingerprint

a25d a255 53bd 8f0b 811e bea2 bfcb c369

Releases are signed with the private key that belongs to this fingerprint. The launcher in your project checks every release against it and refuses to run if anything does not match.

## What is in a release

| File | Purpose |
|---|---|
| `manifest.json`, `manifest.sig` | Release description and its signature |
| `bundle-….json` | The engine and the rules |
| `skye-upgrade-setup.mjs` | One-time setup for a project |

## Support

cesar.carrasco@tinubu.com
