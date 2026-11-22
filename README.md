<p align="center">
  <img src="https://raw.githubusercontent.com/Hearthmakers/.github/main/profile/images/banner.png" alt="Hearthmakers, on a sign over a voxel forest" width="100%" />
</p>

<h1 align="center">Hearthmakers: Releases</h1>

<p align="center">
  The downloads of Hearthmakers, a social voxel game of building and settling, and the files of its website.
</p>

<p align="center">
  <a href="https://github.com/Hearthmakers/Hearthmakers-Releases/releases/latest"><img src="https://img.shields.io/badge/Download-Windows%20%7C%20Linux-2EA043?style=for-the-badge&logo=github&logoColor=white" alt="Download for Windows and Linux" /></a>
  <a href="https://github.com/Hearthmakers/Hearthmakers-Releases/releases?q=android&expanded=true"><img src="https://img.shields.io/badge/Download-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Download for Android" /></a>
  <a href="https://github.com/Hearthmakers/Hearthmakers-Releases/releases?q=server&expanded=true"><img src="https://img.shields.io/badge/Download-Server-6E5494?style=for-the-badge&logo=github&logoColor=white" alt="Download the server" /></a>
  <a href="https://hearthmakers.the-gearfinder.org"><img src="https://img.shields.io/badge/Website%20%26%20Blog-C8792A?style=for-the-badge&logo=rss&logoColor=white" alt="Website and blog" /></a>
</p>

## Play

| Platform | File | Where |
|---|---|---|
| Windows | `Hearthmakers-Setup-<version>.exe` | the [latest release](https://github.com/Hearthmakers/Hearthmakers-Releases/releases/latest) |
| Linux | `Hearthmakers-<version>.AppImage` (make it executable first) | the [latest release](https://github.com/Hearthmakers/Hearthmakers-Releases/releases/latest) |
| Android | `Hearthmakers-<version>.apk` | the [Android releases](https://github.com/Hearthmakers/Hearthmakers-Releases/releases?q=android&expanded=true) |

The apps keep themselves and the game up to date. When a new version is out they ask before installing it, and while you play, a new version of the game downloads quietly and the game asks when to restart.

- **Singleplayer** hosts a world of your own, for playing alone or with your home network.
- **Multiplayer** holds the servers you add by their address, each with its own accounts.

The game is played in the apps only: there is no version for the browser, iPhone, iPad or Mac.

## Host a server

A server is one file, with Node inside: nothing else to install.

1. Download the newest from the [server releases](https://github.com/Hearthmakers/Hearthmakers-Releases/releases?q=server&expanded=true): `hearthmakers-server-windows-x64.exe` or `hearthmakers-server-linux-x64`.
2. Put it in a folder of its own and run it there (on Linux, `chmod +x` it first).
3. Open its port (2567 by default) on your router or firewall for players outside your network.

Players add it in the game's Multiplayer window as `ws://your-address:2567` (or `wss://…` behind a proxy with a certificate).

**Settings** go in a `server.env` file in the same folder, one `NAME=value` per line:

```ini
SERVER_NAME=My Server
SERVER_MOTD=Welcome!
PORT=2567
MAX_PLAYERS=32
```

**The server panel.** When the server starts, its window says a link to a panel in your browser, on that machine only: players, worlds, backups, settings and updates. Type `panel` in the server's window for another link, and `help` for every command.

**Updating.** When a newer server is out, the server says so in its window and its panel. The panel's Update, or `update` typed in the window, downloads it in place of the old one. Players' games always come from the site, so keep the server up to date: a server on another version shows as such in the Multiplayer window.

**Pterodactyl** (Pelican too): import the [Hearthmakers egg](https://hearthmakers.the-gearfinder.org/server/egg-hearthmakers.json) under Admin → Nests → Import Egg. Its settings are the egg's variables, with no `server.env`.

**Plugins** make a server your own: commands, rules, rewards and windows. Put a plugin's folder in a `plugins` folder beside `server.env` and restart. The [Plugin API docs](https://github.com/Hearthmakers/Hearthmakers-Docs) say how to write one.

## The releases

| Release | Tag | What it holds |
|---|---|---|
| Hearthmakers `<version>` | `v<version>` | The desktop app for Windows and Linux. Always the one marked **Latest** |
| Hearthmakers for Android `<version>` | `android-<version>` | The Android app |
| Server `<date>` (`<commit>`) | `server-<commit>` | The server for that version of the game, for Windows and Linux x64. The last 10 are kept |

## The website

[hearthmakers.the-gearfinder.org](https://hearthmakers.the-gearfinder.org) is this repository on GitHub Pages:

- **The root** is the development blog, in English and in Portuguese (`pt-br/`). Its sources are in `content/`.
- **`desktop/game/`** holds the game's files that the apps download: a manifest, each file by its hash, and the versions.
- **`server/egg-hearthmakers.json`** is the Pterodactyl egg.

The game's files, the egg and the releases are published automatically at every release of the game, so `desktop/` and `server/` are never changed by hand.

## Community

Follow the development on the [blog](https://hearthmakers.the-gearfinder.org) and talk with the team on [Discord](https://discord.gg/wvG9pxJbRN).

---

<p align="center"><sub>A tribute and homage to Stonehearth. Proudly made with AI.<br />© 2026 The Gearfinder Studios</sub></p>
