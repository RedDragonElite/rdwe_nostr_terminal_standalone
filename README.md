# ◢ RDWE Nostr Terminal ◣

**Red Dragon Web Engine — Standalone Nostr Web Client**

A complete, single-file Nostr client that runs entirely in your browser.
Zero build step. Zero dependencies. Zero tracking. Just open `index.html`.

---

## What It Does

RDWE Nostr Terminal is a **full-featured Nostr web client** packed into one HTML file.
Drop it on any web server, open it locally with `file://`, or host it on GitHub Pages.
It speaks every NIP that matters — and looks like the cyberpunk terminal you always wished Nostr had.

It pairs perfectly with **[RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)** — the recommended NIP-07 browser extension to keep your `nsec` safe.

---

## ⚡ The Recommended Signer

> **Use [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer) for the best experience.**
>
> - Full **NIP-04** + **NIP-44** support (most signers only ship one)
> - Zero external dependencies — every line of crypto is auditable
> - Per-site permission system with "Always allow" memory
> - Built specifically for the RDWE ecosystem
>
> The Terminal works with **any NIP-07 signer** (nos2x, Alby, etc.), but RDWE Signer unlocks every feature including NIP-44 modern encryption and NIP-17 gift-wrapped DMs.

---

## ✨ Features

### Core
- 📡 **Feed** — your follow-graph timeline with media, reposts, articles
- 🌐 **Global Stream** — the raw Nostr firehose (with backpressure & filtering)
- 👤 **Profiles** — full profile view with notes, banner, NIP-05 verification, follower count
- 🧵 **Threads** — proper NIP-10 threading with ancestors and replies
- 🔔 **Notifications** — likes, reposts, mentions, zaps with unread badge
- ✍ **Compose** — Markdown editor with live preview, hashtag autocomplete, NIP-21 mentions
- 🔍 **Search** — NIP-50 server-side search + hashtag filtering + npub/note lookup
- 👥 **Following / Followers** — full social graph with batch profile loading
- 📨 **DMs** — NIP-04 + NIP-44 + NIP-17 gift-wrap (auto-detects best encryption)
- ⚡ **Zaps** — full NIP-57 zap flow with QR code + invoice copy + auto wallet open
- 🔖 **Bookmarks** — NIP-51 encrypted bookmark lists
- 🔇 **Mutes** — NIP-51 mute lists (people + hashtags, public + encrypted)
- 💻 **Terminal** — raw event firehose with grep filter (developer view)
- 📶 **Relay Manager** — NIP-11 info display, NIP-65 outbox routing, AUTH support
- 🔐 **NIP-05 Generator** — generate `nostr.json` for your own domain
- ⚙ **Settings** — encryption preference, autoplay, sensitive content, etc.

### Performance (v3.2.1)
- 🚀 **Virtual scrolling** on every list — handles 10K+ notes without lag
- 🖼 **IntersectionObserver image lazy-load** — only loads images near viewport
- ⚡ **Lazy reaction fetch** — only subscribes to reactions for visible notes
- 📨 **DM pagination** — last 50 messages, scroll-up loads older
- ⏱ **rAF render throttle** — handles firehose without UI thrash
- 💾 **Profile LRU cache** — capped at 1000 entries
- 📺 **Terminal batch flush** — DocumentFragment-based, handles full firehose

### Security & Privacy
- 🔐 Your `nsec` **never enters this app** — all signing via NIP-07
- 🛰 No analytics, no tracking, no telemetry, no phone-home
- 🌐 No CDN dependencies — fonts loaded from Google but app works offline after first load
- 📁 Zero cookies, zero localStorage of sensitive data (only UI prefs)

---

## Installation

### Option 1: Just Run It Locally

```bash
git clone https://github.com/RedDragonElite/rdwe_nostr_terminal.git
cd rdwe_nostr_terminal
# Open index.html in your browser, that's it
```

Or just download `index.html` and double-click it.

### Option 2: Host on GitHub Pages

1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your terminal is live at `https://yourusername.github.io/rdwe_nostr_terminal/`

### Option 3: Drop on Any Web Server

The file is a single self-contained HTML — copy it to your `public_html`, your nginx root, your S3 bucket, your IPFS node. It works everywhere.

```bash
# Apache / nginx
cp index.html /var/www/html/

# Or with python for quick local hosting
python3 -m http.server 8080
# → http://localhost:8080
```

---

## Quick Start

1. **Install [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)** (recommended) or another NIP-07 extension
2. Open `index.html`
3. The header bar will detect your signer and show your npub
4. Click **⚡ MY FEED** to load your timeline
5. Or paste any `npub1…` into the search bar to view someone's profile

---

## NIP Coverage

| NIP | Feature | Status |
| --- | --- | --- |
| NIP-01 | Basic protocol & events | ✅ Full |
| NIP-02 | Contact list / following | ✅ Full |
| NIP-04 | Encrypted DMs (legacy) | ✅ Full |
| NIP-05 | Domain identifiers + generator | ✅ Full + tool |
| NIP-07 | Browser signer integration | ✅ Full |
| NIP-09 | Event deletion | ✅ Full |
| NIP-10 | Reply threading (marked tags) | ✅ Full |
| NIP-11 | Relay information document | ✅ Read |
| NIP-17 | Gift-wrapped private DMs | ✅ Receive |
| NIP-18 | Reposts & quote reposts | ✅ Full |
| NIP-19 | Bech32 entities (with TLV) | ✅ Full (npub/nsec/note/nevent/nprofile/naddr) |
| NIP-21 | `nostr:` URI scheme | ✅ Clickable |
| NIP-23 | Long-form articles | ✅ Read + Publish |
| NIP-25 | Reactions + custom emoji | ✅ Full |
| NIP-27 | Text note references | ✅ Full |
| NIP-30 | Custom emoji | ✅ Display |
| NIP-36 | Sensitive content (CW) | ✅ Display + Publish |
| NIP-42 | Relay AUTH | ✅ Auto-handles |
| NIP-44 | Modern encryption (ChaCha20) | ✅ Full |
| NIP-50 | Search capability | ✅ Auto-detects relays |
| NIP-51 | Mute lists & bookmarks | ✅ Public + encrypted |
| NIP-56 | Reporting | ✅ Full |
| NIP-57 | Lightning Zaps | ✅ Full LNURL flow |
| NIP-65 | Relay list (outbox model) | ✅ Routes by author |
| NIP-89 | Client identification | ✅ Tagged on every event |
| NIP-92 | Media attachments (imeta) | ✅ Parse + emit |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│  index.html — single-file Nostr client (~230KB)             │
│                                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │
│  │ Bech32   │  │ Markdown │  │ Lazy-    │  │ Virtual  │    │
│  │ + TLV    │  │ Renderer │  │ Loader   │  │ Scroll   │    │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │
│                                                             │
│  ┌──────────────────────────────────────────────────────┐   │
│  │  Relay Engine — WebSocket pool, exp. backoff,        │   │
│  │  NIP-42 AUTH, NIP-65 outbox routing                  │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌──────────────────────────────────────────────────────┐   │
│  │  window.nostr (NIP-07) — provided by your signer     │   │
│  └──────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────────┐
│  Nostr Relays (your configured set)                         │
└─────────────────────────────────────────────────────────────┘
```

The whole client is **one HTML file**. No build step. No bundler. No npm. No webpack.
Open the source — every line is yours to read.

---

## Default Relays

The terminal ships with these relays preconfigured:

```
wss://relay.damus.io
wss://nos.lol
wss://relay.primal.net
wss://nostr.wine
wss://offchain.pub
wss://nostr-pub.wellorder.net
wss://relay.nostr.band
wss://relay.snort.social
```

You can add/remove relays anytime via the **📶 RELAYS** tab.
The terminal also reads your NIP-65 relay list from your signer and connects to those automatically.

---

## Browser Support

Tested on:
- ✅ Chromium 120+ (Chrome, Brave, Edge, Vivaldi)
- ✅ Firefox 120+
- ✅ Safari 17+
- ✅ Mobile Safari (iOS 16+)
- ✅ Mobile Chrome (Android)

The UI is fully responsive — touch targets are 34px+, swipe-scrollable tab bar, master/detail DM nav on mobile, safe-area-inset for iPhone notches.

---

## Customization

Want to tweak the cyberpunk look? Edit the CSS variables at the top:

```css
:root{
  --bg:#000;            /* background */
  --red:#ff0000;        /* primary accent */
  --green:#00ff00;      /* secondary accent */
  --cyan:#00ccff;       /* links */
  --yellow:#ffcc00;     /* zaps */
  --purple:#aa44ff;     /* mentions */
  /* … */
}
```

Want different default relays? Find `DEFAULT_RELAYS` in the script block and edit the array.

Want to add features? It's one file. Read it, fork it, ship it.

---

## File Structure

```
rdwe_nostr_terminal/
├── index.html           ← The whole client. That's it.
├── README.md            ← This file
└── LICENSE              ← BFS v6.66
```

Yes really. **One file.**

---

## Performance Benchmarks

Tested with 1000+ events in feed, 500+ profiles in cache:

| Metric | Value |
| --- | --- |
| Initial DOM render | ~30 cards (virtual scroll) |
| Time to interactive | < 200ms after signer detection |
| Memory at idle | ~40MB |
| Memory with full feed loaded | ~80MB |
| Scroll FPS on mobile (1000 notes) | 60fps |
| Image network requests | Only visible + 400px buffer |
| Reaction subscriptions | Only visible cards |

---

## Compatible Signers

Any NIP-07 browser extension will work:

- ⭐ **[RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)** *(recommended)*
- [nos2x](https://github.com/fiatjaf/nos2x)
- [Alby](https://getalby.com/)
- [Flamingo](https://www.getflamingo.org/)
- [Nostore](https://apps.apple.com/us/app/nostore/id1666553677) (iOS)
- [Amber](https://github.com/greenart7c3/Amber) (Android, via NIP-46 bridge)

> **Why RDWE Signer?** It's the only extension that fully implements both NIP-04 *and* NIP-44 with audited crypto. Most signers ship only one. The terminal needs both for full DM compatibility (legacy + modern + gift-wrap).

---

## Development

There is no build step. There is no dev server config. There is no node_modules.

```bash
git clone https://github.com/RedDragonElite/rdwe_nostr_terminal.git
cd rdwe_nostr_terminal
# Edit index.html
# Reload browser
# Done.
```

That's it. That's the workflow.

---

## Contributing

Pull requests welcome. Keep it:
- ✅ Single-file
- ✅ Zero dependencies
- ✅ Zero build step
- ✅ Compatible with offline `file://` use
- ❌ No npm packages
- ❌ No frameworks
- ❌ No CDN imports (except optional Google Fonts)

If you can't fit it in `index.html`, it doesn't belong in this project.

---

## Roadmap

- [ ] Service Worker for full offline support
- [ ] WebRTC video calls (NIP-100)
- [ ] Stream/podcast player (NIP-53)
- [ ] Public chats (NIP-28)
- [ ] Marketplace (NIP-15 / NIP-99)
- [ ] Lightning wallet integration (NWC, NIP-47)
- [ ] More themes (Light mode? Solarized?)

PRs accepted. Add what you need.

---

## Built By

**◢ RD-ELITE ◣** · Red Dragon Web Engine
Crafted with 🔥 by 🌊 for the RDWE project
License: **BFS v6.66 — Black Flag Source 🏴‍☠️**

> *"Zero bloat. Zero bullshit. Built by developers, for developers."*

---

## Related Projects

- 🐉 **[RDWE](https://github.com/RedDragonElite/rdwe)** — The Red Dragon Web Engine itself (PHP 8.5.4+ on IIS + MariaDB)
- 🔐 **[RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)** — Companion NIP-07 Chrome extension

The trinity:

```
   ┌──────────────┐      ┌──────────────┐      ┌──────────────┐
   │     RDWE     │      │  RDWE Nostr  │      │  RDWE Nostr  │
   │   (Engine)   │      │    Signer    │      │   Terminal   │
   │              │      │              │      │              │
   │  PHP / IIS   │      │ Chrome Ext.  │      │  index.html  │
   └──────────────┘      └──────────────┘      └──────────────┘
         🐉                    🔐                    📡
```

---

⚡ 777 ⚡ FREEDOM > CONTROL · QUALITY > PROFIT · COMMUNITY > CORPORATION ⚡ 777 ⚡
