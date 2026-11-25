# NitroCore Aether Releases

Public update channel for NitroCore Aether.

NitroCore clients verify update metadata with an embedded RSA public key, then verify the downloaded release archive against the signed SHA-256 manifest before installation.

## Channel layout

- `updates/stable.json` — signed release metadata
- `updates/stable.sig` — detached RSA-PSS/SHA-256 signature for `stable.json`
- GitHub Releases — versioned `NitroCore-Aether-vX.Y.Z.zip` application packages

The private publisher signing key is **never stored in this repository**. It remains encrypted to the publisher's Windows user account.

This repository intentionally contains no software license for NitroCore source code.
