# Focused verification · 0.7.0

This update uses affected-path smoke checks; no exhaustive regression suite was run.

## Executed

- Production TypeScript/Vite/PWA build. Existing bundle-size warning remains advisory.
- Two focused Node tests: Cloudflare identity/connection-read validation, failed-save behavior, GET-only calls, 0600 credential storage, restoration/redaction, degraded local-origin state and removal; physical-folder/metadata composition, traversal and symlink escape denial. Cloudflare responses are simulated.
- One isolated real media-engine/background-service smoke workflow: four tiny independent TV series under a temporary parent, each with Season 1 and one generated clip; local NFO and local poster fixtures; preservation enabled; four Series identities with independent Season 1 and artwork. Source files were only created in an OS temporary directory, never in real libraries. No literal example folders from the specification were created.
- Actual API checks for admin-only folder/file inspection, exact source context, authorized metadata enrichment, relative media-user tree, traversal denial, avatar persistence, viewer denial of monitoring/inspection and an authenticated video byte-range response.
- Overview diagnostic values distinguish loopback bind/local endpoint from a configured but unverified HTTPS origin. Existing-monitor state is Not configured until authenticated validation succeeds.
- Browser UI at desktop and 390×844: original parent → four series cards, indexed track/detail view, actual 180-second synthetic MP3 playback, redesigned record, paused animation, zero expanded mini-player nodes, zero mobile player/nav gap and zero horizontal overflow. Browser Back returned to the same track detail route at 13 seconds with playback continuing; mobile Back minimized without losing paused position (21 seconds). Existing five mobile destinations remain intact.
- Stopped playback, signed out and cleared the disposable browser app state. The isolated Admin process was fully exited; the same background-service PID remained available. The test LaunchAgent was unloaded and all temporary accounts/databases/media/profile files were removed.

The first fixture launch collided with the installed app because its test-only port configuration was in the wrong location; corrected without changing the running installed app. The focused workflow also exposed and fixed a real scan/revision conflict. A test expectation was corrected because the engine legitimately indexes the parent as a Folder. Its children remained four distinct series. The generated audio fixture was renamed inside the temporary directory because the engine intentionally excludes files named Sample. No real source media was changed.

## Reviewed without claiming additional environment qualification

- React/TypeScript component structure, accessible button labels and loading/error states; shared responsive backup/restore grid; monitor scope/capability copy; source-file previews and provider-selection wiring.
- Existing macOS helper packaging/lifecycle and approved icon pipeline are retained from 0.6. Packaged artifact checks are recorded with the release manifest after packaging.

## Limits

- No real authorized Cloudflare API credential was saved or tested in the app. No tunnel, DNS route, ingress rule or external connector was changed. Control-plane checks used simulated responses; public reachability, lock/display-off and network-loss recovery are not newly qualified.
- TV fixture metadata/artwork came from local NFO/poster files. The existing online lookup flow remains enabled/configurable, but real provider matching for a specific commercial series was not asserted. Ambiguous classifications require review.
- Admin original-file preview is limited by browser codecs; full compatibility playback remains in the Media Center. Provider search does not move files or silently change series parentage.
- 500 children / 50,000 indexed records bound a folder view; truncation is visible. Search/title views remain separately paginated.
- Native Administration's new monitor/backup panels were build-checked and reviewed; a separate native interaction walkthrough was not claimed for this release.
- Unsigned, non-notarized macOS Apple silicon preview. No Windows/Intel/clean-machine distribution qualification. Existing licensing/corresponding-source release gates remain documented.
