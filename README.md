# Otaconskeep Classroom

**Teaching track for ARR stack + Home Assistant + local voice.**

Canonical site: [https://otaconskeep.github.io/classroom/](https://otaconskeep.github.io/classroom/)

[![Site](https://img.shields.io/badge/Site-otaconskeep.github.io%2Fclassroom-39e6c8.svg)](https://otaconskeep.github.io/classroom/)
[![Discord](https://img.shields.io/badge/Discord-Otaconskeep-5865F2.svg)](https://discord.gg/cZDeqECzX)

## What this is

Blog-style lessons in a strict order. On the website, every teaching step has:

- **What's this mean?** — plain-language explanation
- **More detail** — deeper links, diagrams, and operator tips

## Curriculum

1. [01 — Start here: the right order](docs/01-start-here.md) — TRaSH first. Docker second. Don’t start with random YouTube stacks.
2. [02 — Folders, hardlinks, and atomic moves](docs/02-folders-hardlinks.md) — The most important ARR page. One filesystem tree under /data.
3. [03 — qBittorrent, SABnzbd, and Gluetun](docs/03-downloaders.md) — Categories, paths, VPN only where it belongs.
4. [04 — Prowlarr, Sonarr, Radarr, Lidarr](docs/04-arr-apps.md) — One indexer brain. Separate anime from normal TV.
5. [05 — Recyclarr and TRaSH profiles](docs/05-recyclarr.md) — Stop hand-scoring hundreds of Custom Formats.
6. [06 — Plex, Jellyfin, and library tools](docs/06-media-servers.md) — Mount only /data/media. Fix Direct Play before you blame the server.
7. [07 — Home Assistant: learn it in order](docs/07-home-assistant.md) — Devices → integrations → automations. Backups before fancy.
8. [08 — ESPHome, Zigbee, Matter & Thread](docs/08-devices-mesh.md) — Build a mesh backbone. Thread tip for Kwikset locks.
9. [09 — Local voice: Assist, Wyoming, Linux Voice Assistant](docs/09-voice.md) — Keep Whisper/Piper. Move satellites off archived wyoming-satellite.

## Master sources

- [TRaSH Guides](https://trash-guides.info/) — ARR master reference (start here, not random YouTube)
- [Servarr Wiki](https://wiki.servarr.com/)
- [Recyclarr](https://recyclarr.dev/)
- [Home Assistant docs](https://www.home-assistant.io/docs/)
- [Linux Voice Assistant](https://github.com/OHF-Voice/linux-voice-assistant) — modern Pi satellite path (wyoming-satellite is archived)

## Highlight tip

**Kwikset / Thread locks:** many Matter locks need a working **Thread border router** on your LAN. Home Assistant seeing Wi-Fi is not enough for Thread-only pairing. See [Lesson 08](docs/08-devices-mesh.md).

## License

MIT — Antonio G. Garcia (Otaconskeep)
