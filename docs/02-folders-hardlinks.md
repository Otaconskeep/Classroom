# Lesson 02: Folders, hardlinks, and atomic moves

_The most important ARR page. One filesystem tree under /data._

If downloads and library folders live on different Docker mounts that look like different filesystems, torrents cannot hardlink and Usenet cannot atomic-move cleanly. You waste disk and imports get slow or duplicated.

## Standardize on one tree

Use one parent path (often called /data). Put torrents, usenet, and media underneath it. The word /data is not magic — the shared parent and consistent container paths are.

**What's this mean?** Keep all the boxes in one closet. If downloads live in one closet and movies in another building, the computer cannot make a cheap second name for the same file. It has to copy the whole movie again.

**More detail:** <pre class="cr-tree">/data
├── torrents
│   ├── movies
│   ├── tv
│   ├── anime
│   └── music
├── usenet
│   ├── incomplete
│   └── complete
│       ├── movies
│       ├── tv
│       ├── anime
│       └── music
└── media
    ├── movies
    ├── tv
    ├── anime
    └── music</pre>

## Docker mounts that stay honest

Give Sonarr/Radarr the whole /data. Give qBittorrent only /data/torrents. Give SAB only /data/usenet. Give Plex/Jellyfin only /data/media. Do not mount separate /downloads + /movies + /tv as siblings that Docker treats as different filesystems.

**What's this mean?** Each app only opens the drawers it needs. The librarians see the whole cabinet. The torrent app only sees the download drawer. The TV app only sees finished shows.

**More detail:** TRaSH warns that separate /downloads, /movies, /tv mounts often break hardlinks because Docker presents them as different filesystems even on the same disk.

## Hardlinks (torrents) and atomic moves (Usenet)

Torrents: Sonarr/Radarr can hardlink from the torrent folder into /data/media so one file has two directory entries and seeding continues without a second full copy. Usenet: atomic move means the finished file is renamed/moved into the library on the same filesystem in one step.

**What's this mean?** A hardlink is like two sticky notes pointing at the same homework page. You did not photocopy the page. Atomic move is like sliding a finished paper into the graded folder without leaving a messy half-file behind.

**More detail:** Read TRaSH File &amp; Folder Structure and Hardlinks + Atomic Moves before you import a single movie. Fixing this later means moving terabytes.

## Sources

- [TRaSH File & Folder Structure](https://trash-guides.info/File-and-Folder-Structure/)
- [Hardlinks + Atomic Moves](https://trash-guides.info/Hardlinks/)
- [Docker folder setup](https://trash-guides.info/Hardlinks/How-to-setup-for/Docker/)
