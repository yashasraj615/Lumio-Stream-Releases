# Lumio Stream 0.8.3

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Fix oversized fallback disc artwork on the desktop Music Overview. A desktop-only selector bounds the disc to 190–340px, capped at 35% of the summary container, leaving the existing title, metadata and actions visible.
- Shared disc styling, compact/expanded music players and existing mobile Music Overview rules are unchanged. No backend behavior, library or playback changes.

Focused verification covers the actual desktop overview, TypeScript/Vite/PWA build, DMG integrity and distribution-asset checks. This is not an exhaustive playback/device test. Existing preview and platform qualification limits remain.
