# Lumio Stream 0.8.4

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Fix the oversized decorative disc on Music collection pages by restoring its intended 36px size with a scoped selector. Title-detail and player layouts are retained.
- Remove Download original from all media-information views. Dedicated media-download and original-file routes are denied globally, including native administrators and saved old URLs. Media Center identities advertise downloading as disabled.
- Remove native download controls/context menus from audio/video preview surfaces. Normal playback, seeking, adaptive streams and subtitles remain available. These restrictions remove file-export features; they do not provide DRM or prevent recording/capturing playable streams.

Focused checks cover the actual collection layout and media information, global route denial, playback-route allowlists and the production build/package. No broad playback test was performed. Public distribution contains only the macOS installer, checksum and manifest.
