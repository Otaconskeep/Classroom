# Lesson 04: Prowlarr, Sonarr, Radarr, Lidarr

_One indexer brain. Separate anime from normal TV._

Prowlarr owns indexers. Sonarr/Radarr/Lidarr own libraries. Keep anime on its own TRaSH-aware profile path (Sonarr v4).

## Prowlarr is the indexer hub

Add indexers once in Prowlarr and sync apps. Do not maintain separate indexer lists inside every ARR app.

**What's this mean?** Prowlarr is the shared phone book. Sonarr and Radarr call the same book instead of each keeping a messy paper copy.

**More detail:** <div class="cr-flow">Prowlarr → Sonarr / Radarr / Lidarr → qBittorrent / SABnzbd → /data/media → Plex / Jellyfin</div>

## Sonarr + Radarr basics

Connect download clients with the category paths from Lesson 03. Point root folders at /data/media/tv and /data/media/movies. Confirm hardlink/atomic-move settings after the shared /data mount is correct.

**What's this mean?** Tell each librarian which shelf is theirs and which mail slot brings new books. If the shelf path is wrong, they file copies in the wrong room.

**More detail:** Official Servarr wiki for each app. Verify a test import creates a hardlink (same inode) on Linux when using torrents.

## Anime is not normal TV

Use TRaSH’s dedicated Sonarr Anime configuration. Do not blindly merge anime into your normal WEB-1080p TV profile. Sonarr v4 is required for current anime guide material.

**What's this mean?** Anime naming and release groups play by different rules. Mixing them with normal shows is like filing comic books using a cookbook index.

**More detail:** TRaSH Sonarr Anime Profile. Keep a separate category and folder under /data/.../anime.

## Sources

- [TRaSH Prowlarr](https://trash-guides.info/Prowlarr/)
- [TRaSH Sonarr](https://trash-guides.info/Sonarr/)
- [TRaSH Radarr](https://trash-guides.info/Radarr/)
