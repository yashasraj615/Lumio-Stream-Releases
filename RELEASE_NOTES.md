# Lumio Stream 0.11.4 · Windows fixes: no console window, simpler preserved folders

A Windows x64 fix release. Mac stays at 0.11.0, the Android and Android TV clients at 0.11.1, and Linux at 0.11.2.

## No more terminal window

On Windows 11, where Windows Terminal is the default terminal, a terminal window titled `…\vendor\jellyfin\jellyfin.exe` stayed open while Lumio ran, and closing it stopped the media server. The media engine now runs in an invisible console that has no window at all. Lumio still shuts the engine down cleanly so your library database is never cut off mid-write.

## Preserve existing folder structure just works

Ticking **Preserve existing folder structure** for a TV library no longer asks you to rearrange or classify folders. Libraries that mix series with franchise folders (for example `Friends S1 to S10` next to `Ben 10/Ben 10 Alien Force/…`) save as they are. Names like `Show S1`, `Show Season 1`, `Episode 1` and `Ep. 1` are recognised. The Media Center shows your folders exactly as they are on disk.

## Upgrading

Run `Lumio-Stream-Windows-v0.11.4.exe`. It upgrades 0.11.x in place and keeps your library, accounts, history, tunnel and public address. The installer is unsigned, so SmartScreen may show an unknown publisher; verify the SHA-256 in `SHA256SUMS.txt` first.

---

# Lumio Stream 0.11.3 · Windows update: simpler Cloudflare connection

This Windows x64 update makes remote access setup a clear two-step flow. Mac stays at 0.11.0, the Android and Android TV clients at 0.11.1, and Linux at 0.11.2.

## Connections, one step at a time

1. **Connect your Cloudflare tunnel.** Create a tunnel in Cloudflare, copy the Windows installation command it shows (for example `cloudflared.exe service install eyJ…`) and paste it. Lumio reads only the token from it (the command is never executed), starts its own bundled cloudflared without administrator rights, and waits until Cloudflare has registered the connector for that exact tunnel.
2. **Add your public address.** This step opens once the tunnel is connected. Add a public hostname route in Cloudflare (service type HTTP, URL `127.0.0.1:3615`). Lumio notices the route within seconds and fills in the address. Connect & verify saves it only after the public HTTPS request reaches your own server. Otherwise it explains what to fix and keeps your previous address.

## Also in this update

- A new hostname no longer shows as failing just because your router still caches it as "does not exist": the check also asks Cloudflare's and Google's public DNS resolvers.
- If Lumio's bundled cloudflared is missing (for example removed by antivirus), Lumio downloads the official pinned version and accepts it only if its SHA-256 matches.
- If you already installed cloudflared as a Windows service by following Cloudflare's instructions, Lumio uses it when it runs the same tunnel. Otherwise Lumio offers to stop and disable it (with a Windows administrator prompt; nothing is deleted).
- Full Windows paths such as `"C:\Program Files (x86)\cloudflared\cloudflared.exe" …`, and the bare token, are accepted. Pasting the same command again does not interrupt a working connection.
- Clear messages when Cloudflare rejects a token, a tunnel was deleted, or a firewall blocks the connector.

## Upgrading

Run `Lumio-Stream-Windows-v0.11.3.exe`. It upgrades 0.11.0 in place and keeps your library, accounts, history, saved tunnel and public address. The installer is unsigned, so SmartScreen may show an unknown publisher; verify the SHA-256 in `SHA256SUMS.txt` first.

---

# Lumio Stream 0.11.2 · Linux server edition

Lumio Stream now runs on Linux desktops and headless servers, with the same media server, Media Center, Administration and features as the Mac and Windows editions. Mac and Windows stay at 0.11.0; the Android and Android TV clients stay at 0.11.1 and connect to a Linux server the same way.

## Three ways to install (x86_64)

- **AppImage** (`Lumio-Stream-Linux-v0.11.2-x86_64.AppImage`) for most distributions: make it executable and run it.
- **Debian / Ubuntu** (`Lumio-Stream-Linux-v0.11.2-amd64.deb`): `sudo apt install ./Lumio-Stream-Linux-v0.11.2-amd64.deb`
- **Fedora / RHEL** (`Lumio-Stream-Linux-v0.11.2-x86_64.rpm`): `sudo dnf install ./Lumio-Stream-Linux-v0.11.2-x86_64.rpm`

## What's in the Linux edition

- The background server runs as a per-user systemd service: it starts when you sign in, restarts after a crash and keeps running when Administration closes. No root daemon and no administrator password for the service itself.
- **Start at boot for servers**: `lumio-stream server at-boot on` (systemd linger), or the same switch in Administration → Application.
- A panel tray with server status, Open Media Center, Administration, scan, start/restart/stop, logs and quit, on desktops with a system tray.
- **Headless servers**: `lumio-stream server setup | status | start | stop | restart | logs | backup | restore | quit | remove`, plus `lumio-stream server admin`, which opens Administration in any browser through a one-time local link (works over an SSH tunnel).
- Hardware video encoding detection for VA-API (Intel and AMD), Intel Quick Sync and NVIDIA NVENC, with software fallback.
- Library data lives in `~/.local/share/lumio-stream`; upgrades keep it, and removing the package keeps your library and original media.
- Remote access through Cloudflare works the same as on Mac and Windows, including a system `cloudflared` service.

Guide: https://lumio-stream.pages.dev/docs/linux/

Limitations: tested on Ubuntu 24.04 (desktop session), Debian 12 and Fedora 41 (headless); physical GPUs were not qualified; x86_64 only; packages are unsigned, so verify the SHA-256 before installing.

---

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
