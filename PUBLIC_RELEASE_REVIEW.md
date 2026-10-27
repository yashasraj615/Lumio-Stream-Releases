# Distribution security cleanup · 27 October 2026

Audited all six published releases, v0.5.0, v0.6.0, v0.7.0, v0.8.0, v0.8.1 and v0.8.2. Removed six manually uploaded application-source snapshots, the v0.8.1 runtime-source bundle, two source-index attachments and one source-availability attachment. Current-branch source-index and availability documents were removed. Checksums, manifests and release descriptions were corrected.

The runtime bundle was inspected, including its three nested Jellyfin server, Jellyfin Web and Jellyfin FFmpeg source archives. It was removed under the installer-only distribution policy. The six existing DMGs and their original hashes are retained; no installer was rebuilt or replaced. Bundled third-party licenses/notices are preserved. Existing redistribution qualification limitations remain; this cleanup is not a compliance certification.

All public branches/tags and repository-history file paths were inspected. This repository contains release documents/metadata, not application code. GitHub-generated tag ZIP/tar downloads remain available and contain only that repository content. They do not download from the private application repository. Historical metadata references cannot restore deleted release assets.

The original application's privacy, existing branches and commits are preserved. Only a guarded release uploader, its focused test and publishing documentation are added on mac; main/windows remain unchanged. No Cloudflare, DNS, hosting, deployments or new release publication are part of this cleanup.
