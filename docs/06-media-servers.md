# Lesson 06: Plex, Jellyfin, and library tools

_Mount only /data/media. Fix Direct Play before you blame the server._

Media servers read the finished library. Advanced tools help — after the core is correct.

## Plex / Jellyfin calibration

Point libraries at /data/media/... only. Enable hardware acceleration/encoding when available. Disable Plex Relay when you have proper remote access — Relay is bandwidth-limited. Learn Direct Play vs Direct Stream vs Transcode before changing server settings.

**What's this mean?** Direct Play means the TV plays the file as-is. Transcode means the server cooks a new version on the fly — hotter CPU/GPU and more pain. Find why it is cooking before you throw new settings at it.

**More detail:** TRaSH Plex guide + streaming troubleshooting. Check client codec support, subtitles, and bitrate.

## Useful advanced tools (after the core)

Recyclarr · Seerr (Overseerr/Jellyseerr family) · Tautulli · Maintainerr · qbit_manage · cross-seed · Unpackerr · Kometa · Tracearr · qui. Build core first.

**What's this mean?** These are power tools for a finished workshop. Buying twenty power tools will not fix a crooked floor plan.

**More detail:** Ultimate stack target once solid: Prowlarr, Sonarr, Radarr, Lidarr, Bazarr, Recyclarr, Seerr, Tautulli, Maintainerr, qbit_manage, cross-seed, Unpackerr + qBit/Gluetun + SAB + Plex and/or Jellyfin.

## Sources

- [TRaSH Plex](https://trash-guides.info/Plex/)
- [TRaSH third-party apps](https://trash-guides.info/)
