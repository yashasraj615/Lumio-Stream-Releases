# Lumio Stream 0.8.0

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Two-input Cloudflare setup: paste the official installation command and your public HTTPS address. Lumio parses the credential safely, uses its bundled official connector, applies the hostname immediately and manages the child in the persistent server.
- Separate account/process/tunnel/route/local/public checks. Actual HTTPS page and live instance verification catches stale DNS targets, wrong origins and misleading edge-only connectivity.
- Strict local proxy/HTTPS-forwarding validation, secure cookies and exact-origin protection retained. Public checks have bounded timeouts, pinned public DNS resolution and full TLS validation using host trust stores.
- Optional account APIs and manual networking remain in Advanced; no API key is needed for normal connector setup.
- A targeted idle-system-sleep assertion keeps enabled remote access available while allowing display sleep. No global power/security settings are changed.
- Native endpoint copy/open actions follow the running public URL immediately. Existing accounts, library metadata/history and media paths are preserved.

See CLOUDFLARE_SETUP.md for setup/migration details and VERIFICATION_REPORT.md for actual checks and limits. Forced sleep, logout/reboot, network outages and provider incidents can still interrupt access. No Windows/Intel or clean-machine Gatekeeper qualification is claimed.
