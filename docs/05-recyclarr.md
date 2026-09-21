# Lesson 05: Recyclarr and TRaSH profiles

_Stop hand-scoring hundreds of Custom Formats._

TRaSH Custom Formats and quality profiles are the source of truth. Recyclarr syncs them on a schedule from Git-controlled YAML.

## Do not invent scores by hand

Use TRaSH Radarr/Sonarr Custom Format libraries and quality profile guides. There is no single universal “best” profile — resolution, HDR, devices, storage, and bandwidth matter.

**What's this mean?** Custom Formats are grading rubrics. TRaSH already wrote good rubrics. Copying homework from the maintained book beats inventing grades at midnight.

**More detail:** <ul><li>Typical homelab set: WEB 1080p TV · WEB/UHD premium TV · Anime profile · HD Bluray+WEB movies · UHD movies · efficient 1080p for kids/background</li><li>Sync tools TRaSH recognizes: Recyclarr, Notifiarr, Configarr, Clonarr</li></ul>

## Recyclarr as your sync engine

Prefer Git-controlled Recyclarr YAML → scheduled sync → Sonarr/Radarr. That is reproducible. Clonarr/Notifiarr GUIs exist if you want a browser UI.

**What's this mean?** Recyclarr is the robot that updates the grading rubrics for you every week so you do not click 150 checkboxes again.

**More detail:** Read Recyclarr docs. Store YAML in git. Start with one profile per library, sync, test a grab, then expand.

## Watch a visual explanation once

IBRACORP’s TRaSH profile videos still help you see what scores do in the UI. Then come back to TRaSH text as the living source.

**What's this mean?** Watch once to understand the picture. Keep the book for the numbers that change over time.

**More detail:** Search IBRACORP TRaSH / Custom Formats on YouTube for the visual walkthrough and follow-up.

## Sources

- [Recyclarr documentation](https://recyclarr.dev/)
- [TRaSH Radarr Custom Formats](https://trash-guides.info/Radarr/Radarr-collection-of-custom-formats/)
- [TRaSH Sonarr Quality Profiles](https://trash-guides.info/Sonarr/)
