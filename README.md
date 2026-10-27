# Lumio Stream Releases

Private installer repository for Lumio Stream. Application source and developer instructions live on [Lumio-Stream/mac](https://github.com/yashasraj615/Lumio-Stream/tree/mac).

## Latest verified preview

[0.7.0 for macOS Apple silicon](https://github.com/yashasraj615/Lumio-Stream-Releases/releases/tag/v0.7.0) — macOS 14 or later. This is an unsigned, non-notarized development preview, not a production-qualified release. Before replacing an app, explicitly quit its server/tray and Administration; your data is retained. Lumio has an independent background service: quitting Administration leaves streaming running. First launch offers per-user service setup. Version 0.7 adds original-folder browsing with metadata, safe source inspection, optional read-only monitoring of existing Cloudflare tunnels, and audio Back/record improvements. Existing connectors can stay in place with monitoring; migration is optional for Lumio-owned lifecycle management. Real Cloudflare credential validation and online metadata-provider matches were not qualified by the fixture checks.

Installers are GitHub Release assets, never ordinary Git commits. Names use the configured application version: `Lumio-Stream-macOS-vX.Y.Z.dmg`. Every verified preview includes `release-manifest.json` (actual version, platform, build date, source commit, checks and limitations), `SHA256SUMS.txt` and concise release notes. Verify the hash before installation. GitHub marks development previews as prereleases; the link above identifies the latest verified preview. An unverified development build must not replace it.

Windows `.exe` installers are planned. No completed or verified Windows release is available. Future names will use `Lumio-Stream-Windows-vX.Y.Z.exe` after actual Windows qualification.

yashas raj
