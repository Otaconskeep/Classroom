# Lesson 01: Start here: the right order

_TRaSH first. Docker second. Don’t start with random YouTube stacks._

Before you install twenty containers, learn the order that keeps media stacks healthy for years. The ARR world has a maintained playbook: TRaSH Guides. Build filesystem → downloader → ARR apps → media server.

## Why TRaSH Guides beat random videos

TRaSH Guides are written next to the Sonarr/Radarr ecosystem and stay updated. YouTube is great for seeing a screen — bad as your only source of truth for folder layouts and Custom Formats.

**What's this mean?** Think of TRaSH like the official school book for media bots. Videos can help you see the buttons. The book tells you the right order so you don’t break the house later.

**More detail:** <ul><li>Read <a href="https://trash-guides.info/" target="_blank" rel="noopener">trash-guides.info</a> as the master reference.</li><li>Then open <a href="https://trash-guides.info/Hardlinks/How-to-setup-for/Docker/" target="_blank" rel="noopener">Getting Started / Docker hardlinks path</a> for install order.</li><li>Official app docs live on the <a href="https://wiki.servarr.com/" target="_blank" rel="noopener">Servarr Wiki</a>.</li></ul>

## The only build order you should follow

1) Filesystem layout · 2) Downloader (qBittorrent and/or SABnzbd) · 3) ARR apps (Prowlarr → Sonarr/Radarr/Lidarr) · 4) Media server (Plex/Jellyfin). Skip ahead and you will fight imports forever.

**What's this mean?** First make a clean filing cabinet. Then add the mail room (downloads). Then add the librarians (Sonarr/Radarr). Last, add the TV (Plex). If you buy the TV first, the papers have nowhere smart to go.

**More detail:** A pretty dashboard with twenty tools on a broken folder layout is still a broken stack. Finish Lessons 02–04 before you touch Recyclarr extras, Maintainerr, or Kometa.

## Learn Docker Compose early

Your ARR stack should be reproducible from Compose files — not a pile of containers you clicked into existence. NetworkChuck’s Docker Compose and Docker networking videos are the right primer before Gluetun.

**What's this mean?** Compose is a recipe card. Next year you can rebuild the whole kitchen from the card instead of remembering every knob you turned.

**More detail:** <ul><li>NetworkChuck: Docker Compose</li><li>NetworkChuck: Docker networking (bridge, user-defined, MACVLAN, IPVLAN)</li><li>Only after that: Gluetun + qBittorrent network_mode</li></ul>

## Sources

- [TRaSH Guides](https://trash-guides.info/)
- [Servarr Wiki](https://wiki.servarr.com/)
