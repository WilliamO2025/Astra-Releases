# Astra Releases

This repository is the public, release-only update channel for Astra Safe.

It is intentionally separate from the mod source. A release contains only:

- the compiled Astra JAR;
- `manifest.json`, signed with Astra's Ed25519 release key;
- release notes and checksums.

The signing private key must never be committed. Astra verifies both the manifest signature and the downloaded JAR's SHA-256 hash before staging an update.

## Bootstrap

The current Safe155 build contains the updater code, but its update URL and public verification key are blank. After this repository has a permanent public GitHub URL, build one bootstrap release with that URL and public key embedded. Every later release can then update automatically.
