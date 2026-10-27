# Focused verification · 0.8.0

Only changed-path checks are required for this update. No broad media regression suite or new media/account fixtures.

- Three focused tests: supported command extraction and shell injection rejection; public URL/address constraints; failure classification for Cloudflare 1033 and another Lumio instance versus verified HTTP 200; existing connector supervision/origin checks and retry behavior.
- TypeScript/Vite/PWA build. Existing bundle-size warning remains advisory.
- Official connector archive checked against GitHub asset digest, extracted and version checked. Certificate/hostname validation remains enabled for live HTTPS probes.
- Live investigation confirmed the local origin was Lumio 0.7.0 on loopback port 3615, while public HTTPS returned Cloudflare HTTP 530 / 1033. The exact hostname's CNAME selected a stale tunnel ID; the current existing tunnel was healthy with four edge connections and the correct HTTP origin route. Only the affected DNS record's target was corrected, preserving tunnel identity, token, ingress configuration and unrelated records.
- After propagation the live hostname returned HTTP 200 and the expected Media Center, including the user's existing authenticated browser session. No new user/account was created and no browser credential was extracted.
- Installed 0.8.0 on the current Mac after a cold backup of the old app and full profile. Installed core files match the packaged source. All four existing library configurations remain byte-for-byte unchanged; the real catalog returns in Administration.
- The simplified saved-credential flow and every connection-check row were exercised in the actual native panel. One Lumio-owned connector is running as a child of the persistent server; the legacy system job is stopped and disabled. Fully quitting Administration preserved the same server and connector processes and public HTTP 200. A controlled media-server restart recovered the connector and the public page/health check against the same server instance. Actual macOS NoIdleSleepAssertion belongs to the server.
- Public HTTPS sign-in and an authenticated Movies page were verified with the existing account. No playback or account creation was needed. The private live handoff report retains the exact hostname, tunnel, DNS correction, backup locations and status screenshot; those machine-specific details are excluded from Git.
- DMG verification is VALID. The release manifest records the source commit, artifact size, SHA-256 and remaining limitations.

No physical display-off/lock, forced sleep, reboot, outage simulation, Windows/Intel or clean-machine Gatekeeper qualification is claimed. The power assertion can be inspected in the live macOS power state; that is not a physical display-off test. Original media is never moved or rewritten. The unsigned/non-notarized preview and existing corresponding-source distribution gates remain documented.
