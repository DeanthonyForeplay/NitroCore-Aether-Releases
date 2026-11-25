# Stable update metadata

NitroCore reads two files from this directory:

- `stable.json`
- `stable.sig`

They are generated together by the trusted publisher tooling. Do not hand-edit either file.

A NitroCore update is accepted only when:

1. `stable.sig` verifies the exact bytes of `stable.json` with the public key embedded in the app.
2. The manifest version is newer than the installed version.
3. The package URL matches the configured NitroCore release repository.
4. The downloaded ZIP matches both the signed SHA-256 digest and signed byte count.

Until the one-time publisher key bootstrap is completed on the trusted Windows publisher PC, this directory intentionally contains no `stable.json` or `stable.sig`.
