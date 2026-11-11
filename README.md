# Lumio Stream Releases

Public installer distribution for Lumio Stream. Application code remains exclusively in the original private Lumio-Stream repository.

## Latest verified preview

[0.11.0 for macOS Apple silicon](https://github.com/yashasraj615/Lumio-Stream-Releases/releases/tag/v0.11.0) — macOS 14 or later. Unsigned, non-notarized development preview. This update improves quality transitions, transcoding, timeline previews, background synchronization, session status and private 30-day Watch History.

Installers are Release assets, never Git commits. Verify the accompanying SHA-256 before installation. On macOS, quit the background server and Administration before replacing the installed app; preserve Application Support data. The background service remains available when Administration is closed.

[0.11.0 for Windows x64](https://github.com/yashasraj615/Lumio-Stream-Releases/releases/tag/v0.11.0) is now available as an offline EXE installer. It uses the same Lumio interface, branding, media library and playback features as the Mac baseline, with native Windows startup, tray, upgrade and uninstaller integration. The initial Windows build is unsigned; SmartScreen may show an unknown publisher. Native Windows Server verification passed; physical consumer GPUs and signing reputation are not qualified.

Run the Windows setup wizard, enable the background host, create your administrator and add your existing Windows media folders. Closing Administration leaves the server running. The uninstaller removes the application and startup registration while retaining library data and original media. No Mac accounts, media or tunnel credentials are bundled. See [release notes](RELEASE_NOTES.md), [verification](VERIFICATION_REPORT.md) and [distribution policy](DISTRIBUTION_POLICY.md).

## Android and Android TV clients

[0.11.1 for Android phones and tablets and for Android TV](https://github.com/yashasraj615/Lumio-Stream-Releases/releases/tag/v0.11.1) — Android 8.0 or later. These apps **connect to** a Lumio Stream server running on your Mac or Windows PC; they do not host media. Install `Lumio-Stream-Android-v0.11.1.apk` on a phone or tablet, or `Lumio-Stream-AndroidTV-v0.11.1.apk` on a TV, enter your server's HTTPS address (Remote access) and sign in. Both stay signed in, play music in the background and update themselves from this page after verifying the checksum and signature. Verify the SHA-256 in that release's `SHA256SUMS.txt` before installing.

Only approved installers, checksums and release metadata are published here. No application-source or runtime-source archives are attached. GitHub's automatic Source code ZIP/tar links remain available and contain only this distribution repository's documents/metadata.

yashas raj
