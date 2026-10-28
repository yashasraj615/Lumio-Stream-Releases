# Lumio Stream 0.9.1

macOS 14+ / Apple silicon · unsigned, non-notarized preview

- Fix Administration returning to Overview on macOS activation. Bringing the running window forward preserves its current route and form state. Last section, folder selection, expanded tree and unfinished declaration edits also restore per administrator.
- Simplify Folder Declarations to Main, Collection and Series. Seasons are inferred inside each series. Legacy season declarations migrate atomically to compatibility metadata, preserving their IDs, folder identities and custom season numbers without changing media files or rebuilding the library.
- Collection Containers infer immediate child series automatically, respect explicit overrides and keep series IDs stable when inferred children are explicitly declared. TV browsing and dedicated responsive collection pages show distinct series, their artwork and readable titles; authorized empty collections explain how to populate them.
- Move the compact Episode Order / Alphabetical selector to the right of the season header. Season/tab context restores when returning to a series. Existing episode ordering preferences are retained.

Focused verification is recorded in the distribution manifest. Video controls, audio boost, music, authentication and Cloudflare/DNS/hosting configuration are unchanged. Public assets are limited to the macOS DMG, checksum and manifest.
