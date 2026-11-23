# Fruiterra Overwatch - content pack

Overwatch artwork for the [Fruiterra Graphics Controller](https://github.com/ThePeachZA/fruiterra-graphics-controller): hero art, hero ban icons, transparent hero cut-outs, hexagonal hero badges, hero roles, map images, and the game-mode, role and side icons.

The controller ships no game artwork of its own, so it works with any esport. This pack adds the Overwatch set to a project.

A content pack holds **artwork only**. It never carries teams, players, talent, tournaments or settings, so installing one cannot disturb a project you are already broadcasting.

## What is in the pack

| Category | Count | What it is |
|---|---|---|
| Hero | 211 | 54 heroes, each with its artwork, its ban icon, its transparent cut-out and (where the art exists) its hexagonal badge |
| Map | 29 | Map images, each linked to its game mode |
| Game mode | 5 | Control, Escort, Flashpoint, Hybrid, Push |
| Role | 3 | Tank, Damage, Support |
| Side | 2 | Attack, Defend |

250 assets in total. Team logos, tournament logos and player portraits are **not** included: those belong to the person running the show, not to the artwork pack.

Every hero carries its **role**, so the hero bans overlay can draw the role hexagon without any further setup. The transparent cut-outs are what the hero bans overlay uses for the full-bleed layout, and the hexagonal badges are the framed portrait it shows in the corner.

## What changed in v2

The artwork did not change. What v2 fixes is the packaging.

| | `v1` | `v2` |
|---|---|---|
| Release tag manifest | 157 assets | 250 assets |
| Release asset manifest | 250 assets | 250 assets |
| Hero transparent cut-outs | yes | yes |
| Hexagonal hero badges | yes | yes |
| Hero roles | yes | yes |

The `v1` tag pointed at an older manifest while the `v1` download already carried the newer one,
so the tag and the file disagreed about what the release was. `v2` tags the commit that holds
the manifest the download actually ships, and the release notes match the download.

`v1` stays where it is, for anyone who already links to it. Install `v2` for anything new.

## Installing it

### From the app (easiest)

1. Open the controller and go to **Assets**.
2. Open the **Content packs** panel.
3. Choose **Import pack from URL…**.
4. Paste:

   ```
   https://github.com/ThePeachZA/fruiterra-overwatch/releases/download/v2/fruiterra-overwatch-pack-v2.zip
   ```

5. Press **Install**.

Installing a pack only adds artwork. Your teams, players, tournaments, settings and the running match are never touched. An asset that is already installed is left alone, except that a link which no longer resolves - for example a map that pointed at an icon the app used to bundle - is repaired from the pack.

### From a download

1. Download the release asset `fruiterra-overwatch-pack-v2.zip`.
2. Unzip it.
3. In the controller go to **Assets → Content packs → Import pack…** and pick the folder that holds `pack.json`.

## Building a pack of your own

Every controller can export its own artwork as a pack: **Assets → Content packs → Export pack…**.

A pack is a folder with two things:

```
pack.json                  the manifest: the metadata and one entry per asset
blobs/<xx>/<hash>.<ext>    the artwork, addressed by the SHA-256 of its bytes
```

The app verifies every file against its SHA-256 before it installs anything, so a pack cannot smuggle in a file that is not what the manifest describes.

The `icons/` folder in this repository holds the source PNGs for the game-mode, role and side icons. They are included in the pack as ordinary assets; the folder is here so the icons can be reused or re-coloured.

## Licence and attribution

Overwatch is a trademark of Blizzard Entertainment.

This pack is community artwork provided for personal broadcast use. It is not affiliated with, sponsored or endorsed by Blizzard Entertainment. The artwork in this repository belongs to its respective owners; the repository only distributes it for the convenience of people running the Fruiterra Graphics Controller.
