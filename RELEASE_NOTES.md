# Lumio Stream 0.9.0

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Video controls now fade after three seconds of inactivity, return on interaction and stay available when paused, using controls or opening a player panel. Audio-player layouts are unchanged.
- Video volume defaults to 100%, with an optional 0–150% slider and a marked normal-volume baseline. A single Web Audio output graph amplifies the existing video element. Compression is bypassed at normal volume and enabled only for boost; mute remains effective. Video volume is session-only and separate from music volume. Boosting cannot recover already-clipped source audio.
- Administration gains Folder Declarations: browse configured video roots, declare main, collection, series or season containers, reset to automatic, or recover unavailable/moved folders. Declarations persist in the existing content configuration, take precedence in Lumio's logical catalog and retain the engine's media IDs, sources and viewing history. No source-media files are modified.
- Season episode lists and the in-player episode selector share numerical/alphabetical ordering, with per-user browser preferences. Filename numbering, metadata fallback, specials, multipart ranges and unresolved entries use deterministic ordering. Autoplay follows numerical season order.

Focused verification and release qualification are recorded in the distribution manifest. No broad device or playback suite is claimed. Public release assets are limited to the macOS DMG, checksum and manifest.
