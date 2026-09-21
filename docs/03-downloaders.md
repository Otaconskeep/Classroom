# Lesson 03: qBittorrent, SABnzbd, and Gluetun

_Categories, paths, VPN only where it belongs._

Downloaders unpack and fetch. ARR apps rename and import. Never point the downloader’s final folder at your Plex library.

## qBittorrent categories and paths

Use categories like radarr, sonarr, anime, lidarr mapped to /data/torrents/movies, tv, anime, music. Prefer a real forwarded listening port. Disable UPnP/NAT-PMP when you forward manually. Do not treat SOCKS5 as a full encrypted VPN replacement.

**What's this mean?** Categories are labeled mail slots. Movies go in the movie slot. Shows go in the show slot. That way the librarian bots find the right pile every time.

**More detail:** <ul><li>TRaSH qBittorrent master / basic / paths / categories guides</li><li>Control seeding with ARR indexer rules or tools like qbit_manage — not only a global qBit limit</li></ul>

## Gluetun wraps qBittorrent only

Put the torrent client’s network namespace on Gluetun. Publish UI ports on Gluetun, use network_mode: service:gluetun for qBit. Let Gluetun obtain a VPN-forwarded port and update qBit’s listen port. Do not shove the entire ARR stack behind the VPN.

**What's this mean?** Only the noisy download truck drives through the secret tunnel. The librarians and the TV stay on your normal home road. That is safer and easier to fix.

**More detail:** <div class="cr-flow"><span class="hi">Internet</span> → VPN → <span class="hi">Gluetun</span> → qBittorrent<br>ARR apps stay on the LAN bridge</div>Official docs: Gluetun setup, port mapping through Gluetun, VPN port forwarding.

## SABnzbd does download + unpack only

Use /data/usenet/incomplete and /data/usenet/complete with ARR categories. Disable SAB sorting. Sonarr/Radarr own renaming and library folders. Do not make SAB’s complete folder identical to the Plex library.

**What's this mean?** SAB is the unpacking table. Sonarr/Radarr are the people who put books on the right shelf with the right title. Do not let the unpacking table also be the public shelf.

**More detail:** TRaSH SABnzbd guide + basic setup. SSL Usenet providers preferred.

## Sources

- [TRaSH qBittorrent](https://trash-guides.info/Downloaders/qBittorrent/)
- [TRaSH SABnzbd](https://trash-guides.info/Downloaders/SABnzbd/)
- [Gluetun docs](https://github.com/qdm12/gluetun-wiki)
