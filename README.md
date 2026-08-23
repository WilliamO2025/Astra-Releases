# Astra Releases

This repository is the public, release-only update channel for Astra.

It is intentionally separate from the mod source. A release contains only:

- the compiled Astra JAR;
- `manifest.json`, signed with Astra's Ed25519 release key;
- release notes and checksums.

The signing private key must never be committed. Astra verifies both the manifest signature and the downloaded JAR's SHA-256 hash before staging an update.

## Update channel

`manifest.json` points Astra at the newest signed release. The installed mod verifies
the manifest signature, file size, and SHA-256 hash before it stages an update for
the next launch. Release JARs are attached to GitHub Releases and are not committed
to this repository.
