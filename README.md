# Northline Updates

Public update manifests and release metadata for **Northline Desktop Assistant**.

**Northline** is the public product name. This repository was originally created as `Jarvis-updates`; the repository name is legacy update infrastructure until a future rename or replacement is intentionally done.

The private source repository remains `Hiitschase123/Jarvis` for now.

## Channels

- `channels/private-beta/update-manifest.json` — active private-beta update channel for Northline beta builds.
- `channels/private-beta/release-notes.md` — human-readable release notes for the current beta.
- `channels/stable/update-manifest.json` — reserved stable channel.

## Current update source

Use this manifest URL in Northline:

```text
https://raw.githubusercontent.com/Hiitschase123/Jarvis-updates/main/channels/private-beta/update-manifest.json
```

Example:

```powershell
jarvis-cli.exe --set-update-source "https://raw.githubusercontent.com/Hiitschase123/Jarvis-updates/main/channels/private-beta/update-manifest.json" --approve
jarvis-cli.exe --check-updates
```

The current executable names may still use `jarvis-cli.exe` and `jarvis-ui.exe` until packaged binary names are rebranded in the private source repository. Product-facing copy should use Northline / Northline Desktop Assistant.

## What belongs here

- Public update manifests
- Public release notes
- Public checksums and metadata
- GitHub Release assets for beta packages

## What must not be stored here

- Source code
- Environment files
- Tokens or credentials
- Logs, databases, screenshots, or tester data

## Publishing checklist

1. Build the Northline beta package from the private source repo.
2. Create a GitHub Release in this repo.
3. Upload the beta zip and checksum as release assets.
4. Update `channels/private-beta/update-manifest.json` with the exact version, artifact URL, size, SHA256, and release notes.
5. Test from Northline with `--check-updates`, `--download-update --dry-run`, and `--download-update --approve`.

## Naming policy

- Product name: **Northline Desktop Assistant**
- Short name: **Northline**
- Legacy infrastructure names such as `Jarvis-updates`, `jarvis-cli.exe`, and existing beta asset names may remain temporarily for compatibility.
- New user-facing releases should prefer `Northline-<version>-win64.zip` once the private build pipeline is updated.
