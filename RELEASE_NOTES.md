# Lumio Stream 0.11.0

- In-place quality/audio-track transitions preserve playback position, paused state, speed and subtitle choices; cancellation and rollback protect the previous stream.
- Qualified Apple VideoToolbox, efficient software fallback, three-second HLS segments, bounded buffering and sensible legacy-source bitrate/resolution budgets.
- Timeline scene previews on desktop hover and touch scrubbing, reusing native sprite sheets or a bounded asynchronous frame cache.
- Scoped Android selection/tap-highlight suppression on the video surface.
- Silent progress-row refreshes and PiP synchronization without tearing down the application shell.
- Authoritative login/session status with exact-login revocation, expiry, device labels and offline distinction.
- Private profile Watch History for the last 30 days, including completed titles, partial watches and separate rewatches; expiry preserves resume bookmarks.

Apple silicon macOS 14+ preview; unsigned and non-notarized. No media files, authentication architecture, Cloudflare, DNS or hosting configuration changed. See PLAYBACK_RELIABILITY.md for behavior and qualification limits.

## Windows x64 baseline — 8 November 2026

- Same 0.11.0 branded Media Center, Administration, video/music playback and content features as the Mac application; visual styles/player code retained.
- Offline NSIS EXE with a setup wizard, destination selection, Start Menu/Desktop shortcuts, in-place upgrades and a normal Windows uninstaller.
- Per-user native host, Windows tray, crash supervision and a sign-in startup choice retained across reopening/upgrades. No machine-wide service is installed.
- Native Jellyfin/FFmpeg/FFprobe/cloudflared runtimes pinned to official hashes; Windows drive, UNC and Unicode paths, NTFS profile permissions and native backup tools.
- Native installed-app checks cover playback, graceful shutdown, backup preflight, recovery, reinstall and data-preserving removal. The installer contains no test account, private Mac profile or personal media.

Unsigned Windows x64 baseline. Physical consumer GPUs, HDR/DRM and SmartScreen reputation are not qualified. The installed Mac, private Mac source branch and Cloudflare/DNS/hosting settings were not changed.
