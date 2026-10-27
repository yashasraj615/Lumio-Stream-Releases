# Public release review · 2026-10-27

The release repository's 18 committed historical file blobs were inspected for private keys, known credential formats, private filesystem paths, and live connector configuration. No findings were present. Release assets are versioned DMGs, release manifests and SHA-256 files. The current packaged app contains no profile database, local host/tunnel/listening configuration, runtime connection descriptor or environment file. No user library or live profile is included.

The source repository remains private. Only this installer repository is public. Existing v0.5.0, v0.6.0, v0.7.0 and v0.8.0 previews and their original checksums are preserved. The unqualified local 0.4 development artifact is not promoted as a verified release.

These are unsigned, non-notarized previews, not production-qualified software. Bundled component licenses and source-build information remain in each app's third-party notices. Exact upstream Jellyfin source archives are bundled. The additional runtime source archive contains the exact FFmpeg release source, patches and upstream dependency build recipes; dependency source completeness is not certified by this review.

Version 0.8.2: app source snapshot contains tracked source only; fresh public player screenshots use generated silent media with no account identifiers. The real local profile and live connector configuration are excluded. Prior previews remain preserved.
