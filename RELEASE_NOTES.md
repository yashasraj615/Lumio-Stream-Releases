# Lumio Stream 0.6.0

macOS 14+ / Apple silicon · unsigned development preview

- Correct creator credit: **yashas raj**.
- Independent per-user background server and tray; fully quitting Administration preserves streaming. Reopening reconnects to the same service. Explicit Stop and tray Quit retain clear server-stop semantics.
- Optional server-owned Cloudflare supervision with real local-origin and edge-readiness checks, safe token files, bounded retries, synchronized shutdown and duplicate system-connector detection. Existing external connectors require an explicit one-time migration and are not silently modified.
- Validated macOS iconset → Apple iconutil → ICNS pipeline shared with local logo/PWA/tray assets; installer uses the approved Lumio icon.
- Exact mobile navigation: Home, Directory, Playlist, Favorites, Settings. Narrow login no longer uses desktop-sized spacing.
- Top install/update notifications reserve their measured height. Settings always offers installation or accurate browser guidance; dismissal and confirmed installed state remain distinct.
- Expanded audio fills its player viewport and removes the obsolete mini-player reservation. Minimized playback restores only the floating bar above mobile navigation.

No physical lock/display-off, real public Cloudflare tunnel, real browser installation, Windows or clean-machine Gatekeeper qualification is claimed. The existing system Cloudflare service was preserved. See BACKGROUND_SERVICE.md and VERIFICATION_REPORT.md for setup, evidence and limits.
