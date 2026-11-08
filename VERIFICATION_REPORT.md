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
