# Lumio Stream 0.8.1

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Direct music playback now becomes continuous smart shuffle when Shuffle is enabled, without needing a playlist. Existing suggestion ranking prioritizes unheard music across the accessible library, then continues randomly after completion.
- A private per-user completion record avoids treating brief starts as completed listens. Cycle state follows the existing per-user queue persistence. Explicit album/playlist queues retain their normal shuffle behavior.
- Current playback/position is preserved on activation; manual direct selections continue discovery. Missing, unauthorized and failed tracks cannot strand the sequence.

See SMART_SHUFFLE.md for the completion definition and skipped-track behavior. No music test suite was run, as requested. TypeScript/Vite/PWA build and packaged/local version checks are the focused verification. Existing preview/platform and redistribution limitations still apply.
