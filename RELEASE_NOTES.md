# Lumio Stream 0.8.1

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Direct music playback now becomes continuous smart shuffle when Shuffle is enabled, without needing a playlist. Existing suggestion ranking prioritizes unheard music across the accessible library, then continues randomly after completion.
- A private per-user completion record avoids treating brief starts as completed listens. Cycle state follows the existing per-user queue persistence. Explicit album/playlist queues retain their normal shuffle behavior.
- Current playback/position is preserved on activation; manual direct selections continue discovery. Missing, unauthorized and failed tracks cannot strand the sequence.

No music test suite was run, as requested. TypeScript/Vite/PWA build and packaged/local version checks are the focused verification. Existing preview/platform and redistribution limitations still apply.


Distribution downloads are limited to the installer, its SHA-256 checksum and release metadata. Application source archives, runtime-source bundles and source indexes are not distributed here. GitHub's automatic Source code ZIP/tar links contain this release repository's documents/metadata only; they are not the application source.
