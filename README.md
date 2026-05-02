# GiveMyEmoji — Silly Hacks 2020

> **Type a word, get an emoji. Plus a Chrome extension, an Instagram AR filter, and an Insta-bot — all built in one weekend at Silly Hacks.**

![Cover](repository-assets/1.png)

![Hackathon](https://img.shields.io/badge/hackathon-Silly%20Hacks-ff69b4) ![Stack](https://img.shields.io/badge/stack-HTML%20%2B%20JS%20%2B%20Python-yellow) ![Vibe](https://img.shields.io/badge/vibe-deliberately%20silly-orange)

---

## About

**Who:** Team **codeBlooded** — Gyanesh Samanta and Aaishika S. B.
**What:** *GiveMyEmoji* — a multi-surface emoji-finder. Type any word, get the emoji that fits. Shipped as a web app, a Chrome extension, an Instagram AR filter, and an Instagram chat-bot.
**When:** Built at **Silly Hacks** (September 2020).
**Where:** Browser (web app + Chrome extension), Instagram (AR + DM bot).
**Why:** "If it's stupid but it works, it's not stupid." Hackathons should be fun — this one was about over-engineering an emoji search across four totally different platforms in one weekend.

## The Story

The brief at Silly Hacks: build something deliberately silly, but ship it on more than one platform. We picked emoji-search and went four-for-four:

1. **Web app** (`index.html`) — vanilla JS + Bootstrap + AOS animations, backed by an emoji dataset of **~1,800 entries** (`emoji-dataset.json`).
2. **Chrome extension** — same search, in a popup. Quick-copy any emoji while you browse.
3. **Instagram AR filter** — a Spark AR project (`Instagram Filter/GivemyEmoji Filter.arproj`) that overlays emojis on the user's face.
4. **Instagram bot** — a Python `instabot` script (`instabot/insta.py`) that DMs back emojis in response to keywords.

One weekend, four surfaces, one dataset. The web app is the centerpiece — instant fuzzy lookup against the emoji dataset, no backend required.

## Gallery

| Web app | Demo | Mascot |
|---|---|---|
| ![Cover 1](repository-assets/1.png) | ![Cover 2](repository-assets/2.png) | ![Cover 3](repository-assets/3.png) |

| Logo | Emoji preview |
|---|---|
| ![Logo](images/logo.png) | ![Emoji](images/Emoji.PNG) |

---

## Tech Stack

- **Web app:** HTML5, CSS3, vanilla JS, jQuery, Bootstrap 4, AOS animations
- **Data:** static `emoji-dataset.json` (~1,800 entries) + auxiliary `emoji-dataset2.json`
- **Chrome extension:** Manifest V2, popup HTML/JS/CSS
- **AR filter:** Meta Spark AR Studio (`.arproj`)
- **Bot:** Python + [`instabot`](https://github.com/instagrambot/instabot)

## Repo Structure

```
SillyHacks/
├── index.html              # Web app entry
├── script.js / style.css
├── jquery.js
├── emoji-dataset.json      # ~1,800 emoji
├── emoji-dataset2.json
├── dev.html                # Devs-credits page
├── images/                 # Logo + illustrations
├── repository-assets/      # README screenshots
├── Chrome Extension/
│   ├── manifest.json
│   ├── popup.html / popup.js / popup.css
│   └── icon{16,48,128}.png
├── Instagram Filter/
│   ├── GivemyEmoji Filter.arproj
│   └── textures/
└── instabot/
    └── insta.py
```

## Getting Started

**Web app:** open `index.html` in a browser. That's it.

**Chrome extension:**

1. `chrome://extensions/` → toggle Developer Mode.
2. *Load unpacked* → select `Chrome Extension/`.

**Instabot:**

```bash
pip install instabot
cd instabot
python insta.py
```

**AR filter:** open `Instagram Filter/GivemyEmoji Filter.arproj` in [Meta Spark AR Studio](https://sparkar.facebook.com/ar-studio/).

## Contributing

It's a hackathon repo — but PRs adding more emojis to the dataset or porting the extension to Manifest V3 are welcome.

## License

Released for educational and demo use.

## Credits

| Name | GitHub |
|---|---|
| Gyanesh Samanta | [@GyaneshSamanta](https://github.com/GyaneshSamanta) |
| Aaishika S. B. | [@aaishikasb](https://github.com/aaishikasb) |

Built at **Silly Hacks 2020** by Team codeBlooded.
