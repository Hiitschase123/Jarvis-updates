# Northline Desktop Assistant 0.1.1-beta.7

Private beta channel notes.

This release was originally published with legacy Jarvis artifact names for compatibility. The product name is now **Northline Desktop Assistant** and the short name is **Northline**.

## Highlights

- Prompted beta update delivery flow.
- Manifest v2 support.
- SHA256 artifact verification.
- System Doctor update status.
- Support bundle update metadata.
- Packaged UI update-flow smoke coverage.

## Install / update

1. Download the beta zip from the matching GitHub Release asset.
2. Verify SHA256 using Northline or the `.sha256` file.
3. Close Northline.
4. Extract the new zip to a fresh folder or replace the old beta folder manually.
5. Run `jarvis-cli.exe --readiness` from the new folder.

Northline does not silently install, unzip, replace, or restart itself.

## Known limitations

- No self-install/self-restart by design.
- No license enforcement yet.
- No account login yet.
- Update manifest is public; release assets in this repo are public.
- Signature verification is advisory/schema-level unless explicitly configured later.
- Some compatibility names still say Jarvis until the private build pipeline finishes the full packaged rebrand.
