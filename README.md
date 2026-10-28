# Lumio Stream Releases

Public installer distribution repository for Lumio Stream. Application source stays in the private original Lumio-Stream repository.

## Latest verified preview

[0.9.0 for macOS Apple silicon](https://github.com/yashasraj615/Lumio-Stream-Releases/releases/tag/v0.9.0) — macOS 14 or later. This is an unsigned, non-notarized development preview, not a production-qualified release. Before replacing an app, explicitly quit its server/tray and Administration; your data is retained. Lumio has an independent background service: quitting Administration leaves streaming running. First launch offers per-user service setup. Version 0.9.0 adds fading video controls, optional audio boost up to 150%, Folder Declarations and episode sorting. Version 0.8 introduced managed Cloudflare setup and end-to-end connection checks. See the release notes for qualification limits.

Installers are GitHub Release assets, never ordinary Git commits. Names use the configured application version: `Lumio-Stream-macOS-vX.Y.Z.dmg`. Every verified preview includes `release-manifest.json` (actual version, platform, build date, source commit, checks and limitations), `SHA256SUMS.txt` and concise release notes. Verify the hash before installation. GitHub marks development previews as prereleases; the link above identifies the latest verified preview. An unverified development build must not replace it.

Windows `.exe` installers are planned. No completed or verified Windows release is available. Future names will use `Lumio-Stream-Windows-vX.Y.Z.exe` after actual Windows qualification.

yashas raj

## Distribution boundaries

Only approved installers, installer checksums and necessary release metadata are distributed here. See [distribution policy](DISTRIBUTION_POLICY.md) and [cleanup record](PUBLIC_RELEASE_REVIEW.md). No application-source or runtime-source downloads are provided. GitHub’s automatically generated Source code ZIP/tar links snapshot this distribution repository’s documents/metadata; they do not expose the private application repository.
