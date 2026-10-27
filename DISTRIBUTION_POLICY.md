# Public distribution policy

Lumio-Stream-Releases distributes approved macOS DMG installers, future qualified Windows EXE installers, installer-only SHA-256 files and necessary release metadata. Application code remains in the private Lumio-Stream repository. Do not attach source archives, source snapshots, runtime-source bundles, source indexes, broad directory uploads or arbitrary ZIP/tar files.

Publishing uses the guarded distribution uploader maintained in the private application's mac branch. It validates explicit filenames, installer format markers, sizes and checksums, rejects extra/symlink files and source references, audits the public tag tree and uploads only to an existing unpublished draft. It never creates tags/releases or publishes drafts. A separate owner-authorized review is required before publication. No automatic publishing workflow is enabled by this cleanup.

GitHub automatically adds ZIP/tar links for repository tags. They cannot currently be disabled with a supported repository setting; they contain this repository's release documents and metadata. The application's private repository and tags must never be copied or pushed here.

The two tags that held old source-index/availability metadata are updated to clean distribution snapshots. Historical Git commits remain metadata-only and may retain old references; deleted uploaded archives are not part of Git history.
