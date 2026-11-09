# JUNKYARD JUMPER
### An archived indie game project by Hollowbyte Studios

Junkyard Jumper is a 2D momentum-based endless runner featuring procedural level generation, survival mechanics, unlockable gameplay elements and a junkyard-inspired setting.

This project is no longer under active development and is being released as **open source** for developers, hobbyists and anyone interested in exploring, learning from or building upon the project.

---

## OPEN-SOURCE & ATTRIBUTION

Junkyard Jumper is an open-source project. You are welcome to study its code, modify it, experiment with it and build upon its existing work, subject to the project's licence.

**Attribution is required.**

If you redistribute this project, publish a modified version, use its code in another project, or release a derivative game based on it, you must provide clear credit to the original creator.

The following attribution line must be included:

> Originally created by Aleksandar Stambolić (Hollowbyte Studios). Based on the original Junkyard Jumper project.

For independently released games or public projects, attribution should appear in the credits, README, project description or another clearly visible location.

Please do not claim the original project or its work as entirely your own.

See the accompanying LICENSE file for the applicable usage and redistribution terms.

---

## RUN ON A COMPUTER

**Easiest method:** Double-click `index.html` (works offline; installation and offline caching require a web server).

**With a server (recommended):**

In this folder, run:

```bash
python3 -m http.server 8000
```

Then open:

`http://localhost:8000`

## TEST ON A PHONE

1. Connect your phone and computer to the same Wi-Fi network. Run the server above and find your computer's local IP address (e.g. `192.168.1.20`).
2. On your phone, open `http://192.168.1.20:8000` and rotate to landscape.
3. 'Add to Home Screen' works over HTTP on your local network for a shortcut. Full installation and offline caching require HTTPS (or localhost).

You can also host the folder on a static HTTPS hosting service such as GitHub Pages or Netlify.

**Save data:** Game progress is stored in the browser's localStorage on that specific device and browser. Saves do not automatically sync between devices.

---

## PROJECT FILES

- `index.html` — Main game containing the HTML, CSS and JavaScript.
- `manifest.webmanifest` — Web app manifest.
- `sw.js` — Service worker responsible for offline caching.
- `CHANGELOG.md` — Development changes and updates.
- `QA_REPORT.md` — Quality assurance report.

**Additional information:**
- `backup/` — Contains the previous version of the game, from before the latest development pass.
- `DEATH` constant — Controls the game-over threshold.
- `UNL` — Controls when gameplay mechanics unlock.
- `SAVE_VER` — Save-data version identifier.

**Fonts:** Press Start 2P loads from Google Fonts when online. It falls back to a system monospace font when offline.

---

## RESPONSIVE DESIGN

The game uses a fixed 270px-tall pixel canvas and expands horizontally for wider screens (16:9 up to approximately 2.4:1).

Narrower or taller windows use letterboxing to preserve the original proportions.

The game does not stretch its graphics to fit the screen.

---

## ABOUT HOLLOWBYTE STUDIOS

Junkyard Jumper was developed under **Hollowbyte Studios**, an independent game development studio focused on creating original games and interactive experiences.

Although this project is archived, it remains part of the studio's development history.

### FIND US ONLINE

- GitHub: `HollowbyteStudios`
- YouTube: `Hollowbyte.Studios`
- Instagram: `hollowbyte.studios`
- TikTok: `hollowbyte.studios`
- X (Twitter): `AidenDev`

*Social media handles and links may be updated in the future.*

---

© Hollowbyte Studios. Original project created by Aleksandar Stambolić.
