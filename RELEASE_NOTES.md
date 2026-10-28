# Lumio Stream 0.10.1

- Dedicated Media Metadata administration: catalog search, identity/story/credits/TV ordering, staged provider rematching, explicit save/cancel, stale-edit detection and saved-history restore.
- Missing-artwork scanning and recovery with validated local image caching, reviewable candidates, upload/HTTPS image choices, protected manual selections and progress/retry controls.
- Deterministic immediate-child collection covers and parent-series season fallbacks; existing folder declarations and media files remain intact.
- Collections now query video collections explicitly and reject audio memberships. A targeted repair action removes existing invalid audio relationships without deleting collections or music.
- Authenticated Party Watch in the existing video player: expiring invitations, host play/pause/seek/rate, participant status, reconnect and clock/drift compensation. Invitations grant no media access; restarting Lumio ends parties.
- Existing music covers can appear inside the shared branded spinning disc, with the original fallback and playback-driven rotation.

Apple silicon macOS 14+ preview; unsigned and non-notarized. Artwork availability depends on configured metadata providers. Ambiguous results require administrator review; no artwork or metadata guesses are silently applied. No Cloudflare, DNS or hosting settings changed.

0.10.1 also applies saved artwork consistently to global search, person credits and TV browsing responses.
