# Lumio Stream 0.9.2

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Unify video attenuation, boost and mute in one persistent Web Audio output stage. The native element stays at unity while the gain node applies the selected 0–150% level; mute gates the same output to zero. Reapply intent on native volume/source events without reading transient values into preferences or polling. A native-only fallback supports 0–100% when Web Audio is unavailable.
- Keep the selected video slider level while muted. Slider changes remain silent until Unmute, which restores the selected level; a zero slider can restore the last nonzero level. Session-only video preferences remain separate from music. Existing music volume behavior is retained.
- Add accessible previous/next recommendation arrows to the existing “More from your collection” rail. Each click scrolls one card, with smooth motion, edge disabling, resize tracking and reduced-motion support. Touch and trackpad scrolling remain available.
- Refine mobile video touch targets, timeline spacing, safe areas and settings. Prefer landscape only during supported touch-device fullscreen; gracefully retain playback if orientation locking is unavailable. No video element recreation on rotation.
- Refine mobile sign-in with compact short-screen spacing, proper username input hints, a larger visibility toggle, visual-viewport keyboard clearance and duplicate-submit protection. Existing authentication and route restoration are unchanged. Desktop login styling is retained.

Focused verification and platform limitations are recorded in the distribution manifest. No backend/database, scanner, collection hierarchy, Admin persistence, Cloudflare, DNS or hosting configuration changes. Public assets are limited to the macOS DMG, checksum and manifest.
