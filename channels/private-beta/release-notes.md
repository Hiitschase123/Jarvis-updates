# Jarvis 0.1.1-beta.7

Private beta channel notes.

## Highlights

- Prompted beta update delivery flow.
- Manifest v2 support.
- SHA256 artifact verification.
- System Doctor update status.
- Support bundle update metadata.
- Packaged UI update-flow smoke coverage.

## Install / update

1. Download the beta zip from the matching GitHub Release asset.
2. Verify SHA256 using Jarvis or the `.sha256` file.
3. Close Jarvis.
4. Extract the new zip to a fresh folder or replace the old beta folder manually.
5. Run `jarvis-cli.exe --readiness`.

Jarvis does not silently install, unzip, replace, or restart itself.

## Known limitations

- No self-install/self-restart by design.
- No license enforcement yet.
- No account login yet.
- Update manifest is public; release assets in this repo are public.
- Signature verification is advisory/schema-level unless explicitly configured later.
