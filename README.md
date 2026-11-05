# Clairacte downloads

Public installer-only distribution for Clairacte, the French professional observation and transcription workspace. Development source remains private in the owner's source repository. Matter data, recordings, credentials and signing secrets are never stored here. As with any Electron binary, distributed application code can be inspected; private source hosting is not an obfuscation guarantee.

## Available now: Mac preview

[Download Clairacte 0.6.1 for Apple Silicon](https://github.com/B3ANQ/Clairacte-Releases/releases/download/v0.6.1-mac-preview/Clairacte-0.6.1-mac-arm64.dmg)

[Preview release, checksums and limitations](https://github.com/B3ANQ/Clairacte-Releases/releases/tag/v0.6.1-mac-preview)

This is an explicitly labelled Mac-only preview. All 14 local verification stages passed, including 66 automated tests and a clean runtime/development audit. Update recovery and PDF/DOCX metadata defects were fixed; exported pages were rendered and reviewed. The corrected Mac installer was installed/launched and checked locally. The DMG and ZIP passed integrity checks; actual bundled French speech recognition passed. A Windows 0.6 installer and the complete stable feed have not been published because GitHub's source-repository workflow attempts failed before starting jobs. No complete two-platform test success is claimed.

Quit the old app, open the DMG, drag Clairacte into Applications and launch it there. Keep an encrypted backup before upgrading. The ZIP is an updater archive; ordinary installation uses the DMG. Transcription is free, offline and uses bundled whisper.cpp, with no API key or subscription.

## Updates and publisher trust

The 0.6 application includes French update controls and strict Ed25519/size/hash/version verification for future stable releases. Existing 0.5.x installations need a manual updater-enabled upgrade once. This prerelease is intentionally excluded from the stable update feed; until a complete stable version is published, checking can report that the feed is unavailable.

Future stable releases require both native build/test jobs to pass. Automatic public publication also requires a dedicated restricted publishing token in the private source repository; it has not yet been configured. No private development credential is embedded in the app or public CI.

The Mac preview is ad hoc signed, without Apple Developer ID/notarization; macOS may show its verification warning. Windows publisher signing is also not configured. Signing identities and notarization credentials must be supplied by the publisher before trusted distributions can be built. Even signed new Windows binaries can encounter SmartScreen reputation warnings. No system-security bypass, security certification or malware-free guarantee is claimed.
