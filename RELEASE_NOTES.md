# Lumio Stream 0.11.0

- In-place quality/audio-track transitions preserve playback position, paused state, speed and subtitle choices; cancellation and rollback protect the previous stream.
- Qualified Apple VideoToolbox, efficient software fallback, three-second HLS segments, bounded buffering and sensible legacy-source bitrate/resolution budgets.
- Timeline scene previews on desktop hover and touch scrubbing, reusing native sprite sheets or a bounded asynchronous frame cache.
- Scoped Android selection/tap-highlight suppression on the video surface.
- Silent progress-row refreshes and PiP synchronization without tearing down the application shell.
- Authoritative login/session status with exact-login revocation, expiry, device labels and offline distinction.
- Private profile Watch History for the last 30 days, including completed titles, partial watches and separate rewatches; expiry preserves resume bookmarks.

Apple silicon macOS 14+ preview; unsigned and non-notarized. No media files, authentication architecture, Cloudflare, DNS or hosting configuration changed. See PLAYBACK_RELIABILITY.md for behavior and qualification limits.
