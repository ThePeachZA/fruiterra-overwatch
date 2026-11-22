# Fruiterra Overwatch — content pack

Overwatch artwork for the [Fruiterra Graphics Controller](https://github.com/ThePeachZA/fruiterra-graphics-controller): hero art and ban icons, map images, team logos, player portraits, and the game-mode, role and side icons.

The controller ships no game artwork of its own, so it works with any esport. This pack adds the Overwatch set to a project.

## What is in the pack

| Category | Count | What it is |
|---|---|---|
| Hero | 108 | Hero art and its small ban icon |
| Map | 29 | Map images, each linked to its game mode |
| Logo | 6 | Team logos |
| Portrait | 4 | Player and talent portraits |
| Game mode | 5 | Control, Escort, Flashpoint, Hybrid, Push |
| Role | 3 | Tank, Damage, Support |
| Side | 2 | Attack, Defend |

## Installing it

### From the app (easiest)

1. Open the controller and go to **Assets**.
2. Open the **Content packs** panel.
3. Choose **Import pack from URL…**.
4. Paste:

   ```
   https://github.com/ThePeachZA/fruiterra-overwatch/releases/download/v1/fruiterra-overwatch-pack-v1.zip
   ```

5. Press **Import**.

Installing a pack only adds artwork. Your teams, players, tournaments, settings and the running match are never touched. An asset that is already installed is left alone, except that a link which no longer resolves — for example a map that pointed at an icon the app used to bundle — is repaired from the pack.

### From a download

1. Download the release asset `fruiterra-overwatch-pack-v1.zip`.
2. Unzip it.
3. In the controller go to **Assets → Content packs → Import pack…** and pick the folder that holds `pack.json`.

## Building a pack of your own

Every controller can export its own artwork as a pack: **Assets → Content packs → Export pack…**.

A pack is a folder with two things:

```
pack.json          the manifest: the metadata and one entry per asset
blobs/<xx>/<hash>.<ext>   the artwork, addressed by the SHA-256 of its bytes
```

The app verifies every file against its SHA-256 before it installs anything, so a pack cannot smuggle in a file that is not what the manifest describes.

## Licence and attribution

Overwatch is a trademark of Blizzard Entertainment.

This pack is community artwork provided for personal broadcast use. It is not affiliated with, sponsored or endorsed by Blizzard Entertainment. The artwork in this repository belongs to its respective owners; the repository only distributes it for the convenience of people running the Fruiterra Graphics Controller.
