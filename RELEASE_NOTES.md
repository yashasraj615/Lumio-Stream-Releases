# Lumio Stream 0.11.1 · Android and Android TV clients

Two new apps that **connect to** your Lumio Stream server. They do not host, scan or store a media library; your Mac or Windows server stays the home of your collection. Desktop servers remain at 0.11.0.

## Lumio Stream for Android (phones and tablets)

- Enter your server's address, sign in on its own page, and use the same Media Center, theme and features.
- Music plays natively: it continues with the screen locked and moves to the next track like a dedicated music app.
- The notification, lock screen, Bluetooth and car displays show the title, artist and the Lumio record with the album cover, with play/pause, previous, next, seek, favourite, shuffle and repeat.
- Picture-in-picture for video from Back, Home or full screen; Back follows the Media Center's dialogs, players and pages.
- Stays signed in until you sign out, including across server restarts.
- A redesigned connect screen, and the disc label now stays inside its centre on every screen size.

## Lumio Stream for Android TV

- A native interface designed for the remote, in the Lumio look: home with Movie of the day and your rows, side navigation, libraries, series with seasons, albums, search and favourites.
- A film and episode player with direct play when the TV can decode the file and server transcoding otherwise, skip and pause from the remote, subtitles, audio tracks and up next.
- A listening room with the turning Lumio record; music keeps playing in the background.
- Native sign-in that stays signed in until you sign out.

Both apps update themselves from this page: they offer a newer version, verify its checksum and signature, and install it over the current app while keeping your sign-in.

Requirements: Android 8.0 or later, and a Lumio Stream server reachable at its HTTPS address (Remote access) or locally over USB.

Limitations: tested on Android 14 emulators (the TV app at TV resolution with D-pad and media keys), not physical TV or phone hardware; the first self-update needs the one-time "Install unknown apps" permission. Media downloads for offline use are not offered because Lumio servers disable media downloads.

---

# Lumio Stream 0.11.0

- In-place quality/audio-track transitions preserve playback position, paused state, speed and subtitle choices; cancellation and rollback protect the previous stream.
- Qualified Apple VideoToolbox, efficient software fallback, three-second HLS segments, bounded buffering and sensible legacy-source bitrate/resolution budgets.
- Timeline scene previews on desktop hover and touch scrubbing, reusing native sprite sheets or a bounded asynchronous frame cache.
- Scoped Android selection/tap-highlight suppression on the video surface.
- Silent progress-row refreshes and PiP synchronization without tearing down the application shell.
- Authoritative login/session status with exact-login revocation, expiry, device labels and offline distinction.
- Private profile Watch History for the last 30 days, including completed titles, partial watches and separate rewatches; expiry preserves resume bookmarks.

Apple silicon macOS 14+ preview; unsigned and non-notarized. Windows x64 baseline added 8 November 2026. See the v0.11.0 release for details.
