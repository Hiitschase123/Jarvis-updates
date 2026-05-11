# Jarvis Updates

Public update manifests and release metadata for Jarvis private beta builds.

This repository is intentionally separate from the private `Hiitschase123/Jarvis` source repository.

## Channels

- `channels/private-beta/update-manifest.json` — active private-beta update channel.
- `channels/private-beta/release-notes.md` — human-readable release notes for the current beta.
- `channels/stable/update-manifest.json` — reserved stable channel.
- `channels/dev/update-manifest.json` — reserved dev channel.

## Current update source

Use this manifest URL in Jarvis:

```text
https://raw.githubusercontent.com/Hiitschase123/Jarvis-updates/main/channels/private-beta/update-manifest.json
```

Example:

```powershell
jarvis-cli.exe --set-update-source "https://raw.githubusercontent.com/Hiitschase123/Jarvis-updates/main/channels/private-beta/update-manifest.json" --approve
jarvis-cli.exe --check-updates
```

## What belongs here

- Public update manifests
- Public release notes
- Public checksums / metadata
- GitHub Release assets for beta packages

## What must not be stored here

- Jarvis source code
- `.env` files
- tokens or secrets
- logs, databases, screenshots, tester data
- private license keys

## Publishing checklist

1. Build the Jarvis beta package from the private source repo.
2. Create a GitHub Release in this repo, for example `jarvis-0.1.1-beta.7`.
3. Upload the beta zip and checksum as release assets.
4. Update `channels/private-beta/update-manifest.json` with the exact version, artifact URL, size, and SHA256.
5. Test from Jarvis with `--check-updates`, `--download-update --dry-run`, and `--download-update --approve`.
