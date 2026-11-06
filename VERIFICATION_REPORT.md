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
- DMG structure/checksum, arm64 bundle, exact packaged backend/frontend bytes and running local health verified. Publication uploads exactly the DMG, SHA256SUMS.txt and release-manifest.json. Full public-download verification follows publication and is recorded locally.

Limitations: unsigned/non-notarized preview for macOS 14+; no Intel/Windows or clean-machine qualification; no forced hardware-failure or real network-loss injection. Hardware configuration fallback needs an authenticated administrator connection. Existing history cannot reconstruct unrecorded older rewatches.
