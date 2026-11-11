# Lumio Stream 0.11.2 Linux verification

Built from private branch `linux`, commit `2eb75ab8e152b41bd619e809b786b0e83c957e41`, by the private GitHub Actions "Linux baseline" run `43067248394` on Ubuntu 24.04 x86_64. The published files are byte-identical to the packages that run built and verified (SHA-256 checked after transfer). Disposable test accounts and generated media only; no personal library or account was used.

Installed-package checks (real systemd user session, Xvfb display, Google Chrome), all 17 passed:

- The Debian package installs the branded app, launcher, desktop entry and pinned Linux runtime; the rpm and AppImage are well-formed.
- `lumio-stream server setup` installs the systemd user service; the gateway and Jellyfin become healthy.
- Native Administration signs in and renders under X11; closing it leaves the server running and starts the panel tray as its own user unit.
- The real scanner indexes Unicode and space-containing Linux paths without changing original files.
- Supported video uses actual Direct Play in Chrome; legacy video actually transcodes to HLS, and quality changes keep the paused position.
- Timeline scene previews are extracted by the Linux FFmpeg; profile Watch History follows actual playback; music plays with the branded disc.
- Headless Administration works in a browser through the one-time loopback bridge with Linux preferences.
- Clean engine stop/start and tar backup and restore from the terminal.
- A crashed server is restarted by systemd with no orphaned engine.
- Quitting and reopening the background server keeps the sign-in start choice.
- The AppImage runs the same terminal commands against the installed server profile.
- An in-place package upgrade keeps configuration, database and the service registration; removing the package keeps library data and original media and leaves no failing service loop.
- Test data was removed from the runner; the packages contain no seeded account.

Headless containers without systemd or a display: on Fedora 41 (rpm) and Debian 12 (deb), an unprivileged user ran `server version`, `setup`, `status` (ready), `stop` and `quit`.

Limitations: hosted runners only; physical GPUs (VA-API, NVENC, Quick Sync) and physical desktop panels were not qualified; no public Cloudflare tunnel was configured; other distributions were not tested.

# Lumio Stream 0.11.1 Android clients verification

Built from private branch `android`, commit `0ab29af8a5a3ce425f97b1c049f7ca559cf33713`, as minified release APKs signed with the Lumio Stream release key (certificate SHA-256 `1a3ab34249666fb47e15aa4b699eaa30a480703dd8de771e4abe9392a57c1465`). Tested against disposable Lumio 0.11.0 servers with generated media; no personal library or account was used.

- Phone (Android 14 emulator): connect and server sign-in; sign-in kept across server restarts and across an in-place update from an earlier build; album playback with the screen locked advanced track to track while the foreground service stayed active; the system media session carried title, artist, album and the branded disc artwork; favourite was written to the server and shuffle mirrored the page; Back closed dialogs, collapsed players and returned through pages; picture-in-picture from Back, Home and full screen showed only the video, its controls worked and closing it stopped playback.
- TV (Android 14 emulator at 1920×1080, 320 dpi, driven only with D-pad and media keys): connect and native sign-in; home feed with focus-driven hero and backdrop; side navigation; film, series and album pages; search; settings; direct-play video with remote seek and pause and progress reported to the server; music with background playback and track advance after leaving the app.
- Updater: release discovery, SHA-256 and signer verification were exercised against a local releases feed. The final Android install confirmation was not completed.

Limitations: no physical Android TV, Google TV, phone, Bluetooth or long-Doze testing; the TV app was exercised on a phone system image at TV resolution.

# Lumio Stream 0.11.0 verification

- Apple silicon macOS application installed and running, version 0.11.0. Existing five libraries, twelve folder declarations and host settings preserved.
- Production build and twelve focused automated checks passed.
- Real legacy 480p HEVC episode played through VideoToolbox H.264/AAC HLS; 720×480 output and 545 fps encoder throughput were reported. Compatible H.264/AAC MP4 played directly. No long-duration performance benchmark is claimed.
- A paused quality change retained 757.689 seconds exactly, 1.25× speed and selected audio/burned subtitle. Playing and rapid quality changes selected the latest requested quality and continued. Rejected negotiation and post-attachment restoration were covered by a deterministic controller fixture.
- Desktop hover and phone touch scrubbing displayed actual 320×180 decoded scene frames. Phone and tablet emulation showed no text selection or horizontal overflow. Physical Android devices were not tested.
- PiP entry/exit and return Home retained the same page time origin, route context and advancing playback.
- Private profile history displayed actual recent partial and finished titles. Stable viewing identity, rewatches, cross-user isolation and repeatable 30-day expiry were checked in focused fixtures without deleting resume state.
- Administration displayed separate native and Chrome logins. Revoking Chrome changed only that login to Revoked; its next authenticated request returned the sign-in screen. Logout, expiry and offline status were covered by server fixtures.
- Original playback position, speed and quality were restored after playback checks. No test account or test library was created.
- DMG structure/checksum, arm64 bundle, exact packaged backend/frontend bytes and running local health verified. The initial Mac publication uploaded the DMG, SHA256SUMS.txt and release-manifest.json. The Windows baseline adds only its EXE and refreshes the combined checksum/manifest. Full public-download verification follows publication and is recorded locally.

Limitations: unsigned/non-notarized preview for macOS 14+; no Intel Mac or physical consumer-PC qualification; no forced hardware-failure or real network-loss injection. Hardware configuration fallback needs an authenticated administrator connection. Existing history cannot reconstruct unrecorded older rewatches.

## Windows baseline verification

Private native Windows Server 2025 x64 Actions run `42443911339` passed for application build commit `1f9f8b51d6d9d1aedb6deb0a4ee3693a6a20ec73` on the private `windows` branch. Twelve focused checks and fifteen installed-application checks passed:

- Real NSIS installation, final branded GUI/server binary identity and native Administration sign-in; closing Administration retained the server.
- Real scanning of Unicode/space paths, Edge H.264/AAC Direct Play and software HLS transcoding of a legacy MPEG-4/AC-3 source.
- A completed quality transition preserved paused position; an actual FFmpeg timeline preview decoded; history and branded-disc music playback worked.
- Graceful engine stop completed before the force-kill deadline and emitted an orderly-shutdown log. Windows tar backup/restore preflight, start/stop and watchdog crash recovery worked.
- Disabling sign-in startup survived reopening without another installation prompt. In-place NSIS reinstall retained configuration and startup preference.
- The real uninstaller removed application/startup registration while keeping configuration and original video/audio files. Disposable verification profile, user and media were erased from the runner afterward; no seeded account is packaged.
- Administration, video controls/scene preview and music interfaces were visually inspected.

The application remains unsigned. This is native hosted-Windows qualification, not physical consumer GPU, HDR/DRM, SmartScreen-reputation or all-hardware certification. No live Cloudflare tunnel was configured by CI.

The published Windows EXE is 437,358,739 bytes with SHA-256 `4a71c3bd7bb3f115a4b6f751eefe0d3a479f56fa964cf94b3fe67c106b0d65e9`. An unauthenticated HTTP 206 request downloaded a byte range matching the local PE bytes and full Content-Range size; GitHub’s full asset digest matches the locally downloaded installer/CI checksum. Public combined checksums and manifest were downloaded and byte-matched. A second full public EXE download was not required or performed. The Mac DMG retains its original size/hash. The release contains exactly the two installers, checksum file and manifest.
