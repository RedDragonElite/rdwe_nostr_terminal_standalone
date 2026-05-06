# 🐉 RDWE Nostr Terminal

[![Version](https://img.shields.io/badge/version-3.2.3-red?style=for-the-badge)](https://github.com/RedDragonElite/rdwe_nostr_terminal)
[![License](https://img.shields.io/badge/license-RDE%20Black%20Flag-black?style=for-the-badge)](LICENSE)
[![Single File](https://img.shields.io/badge/Single--File-230KB-green?style=for-the-badge)](#)
[![Zero Deps](https://img.shields.io/badge/Dependencies-ZERO-orange?style=for-the-badge)](#)
[![Nostr](https://img.shields.io/badge/Nostr-Decentralized-purple?style=for-the-badge)](https://nostr.com)

**The Cyberpunk Nostr Web Client That Actually Respects Your Intelligence**

*Built by [Red Dragon Elite](https://rd-elite.com) | Free Forever | Single HTML File*

[📖 Documentation](#-installation) • [🚀 Quick Start](#-quick-start) • [⚡ Live Demo](https://rdwe.rd-elite.com) • [🔐 Signer](https://github.com/RedDragonElite/rdwe_nostr_signer) • [🌐 Website](https://rd-elite.com)

---

## 📸 Screenshots

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/799576a9-5939-4290-bb2c-b24d65bc578f" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8dfda4a8-b8b8-4f1b-9e32-e58c4ef696b0" />

The most beautiful Nostr terminal in the world. Cyberpunk red-on-black aesthetic. Glitch effects. Real-time relay status. Live event firehose. **No bullshit.**

---

## 🔥 Why This Client Changes Everything

The current Nostr web client landscape is **broken by design**:

| ❌ Modern Nostr Clients | ✅ RDWE Nostr Terminal |
| --- | --- |
| **300MB node_modules** for "Hello World" | **230KB total** — entire client |
| **Build steps** (webpack, vite, rollup) | **No build** — just open index.html |
| **CDN dependencies** (React, Tailwind, etc.) | **Zero CDN deps** — works offline |
| **Tracking & analytics** baked in | **No phone-home** — ever |
| **Half NIP coverage** | **Full NIP coverage** — 25+ NIPs |
| **NIP-04 OR NIP-44** (rarely both) | **NIP-04 + NIP-44 + NIP-17** |
| **Hidden behind paywalls** | **100% Free Forever** |
| **Framework upgrades break everything** | **Vanilla JS** — runs in 20 years |

### 🎯 Key Features

- 🔓 **Truly Open Source** — Read every line, no obfuscation, no minification tricks
- 📦 **Single File Architecture** — 1 HTML file = the entire application
- 🚀 **Virtual Scrolling** — Handles 10,000+ notes at 60fps on mobile
- 🔐 **NIP-07 First** — Your `nsec` never touches the app
- 💬 **Full DM Stack** — NIP-04 + NIP-44 + NIP-17 gift-wrap (auto-detects)
- ⚡ **Lightning Zaps** — QR codes, COPY-paste, wallet auto-open, full LNURL flow
- 🌐 **Global Firehose** — Watch the entire Nostr network in real-time
- 🔍 **NIP-50 Search** — Auto-detects search-capable relays
- 🎨 **Cyberpunk UI** — Red-on-black terminal aesthetic, glitch effects, scanlines
- 📱 **Mobile First** — 34px+ touch targets, master/detail navigation, safe-area
- 🔖 **Encrypted Bookmarks & Mutes** — NIP-51 lists, public + private
- 🛡️ **Privacy First** — No tracking, no telemetry, no analytics
- 🌍 **Host Anywhere** — GitHub Pages, S3, IPFS, your own server, or `file://`

---

## 🚀 Quick Start

### Option A: Just Run It Locally (60 seconds)

```bash
# Clone or download
git clone https://github.com/RedDragonElite/rdwe_nostr_terminal.git
cd rdwe_nostr_terminal

# Open it
xdg-open index.html       # Linux
open index.html           # macOS
start index.html          # Windows

# That's it. You're running a full Nostr client.
```

Or just **download `index.html`** and **double-click it**. Done.

### Option B: Host on GitHub Pages (5 minutes)

1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your terminal goes live at `https://yourusername.github.io/rdwe_nostr_terminal/`

### Option C: Drop on Any Web Server

```bash
# Apache / nginx
cp index.html /var/www/html/

# Or quick Python local hosting
python3 -m http.server 8080
# → http://localhost:8080
```

The file is **self-contained**. Copy it anywhere — it works everywhere.

---

## 🔐 The Recommended Signer

> **Use [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer) for the best experience.**

The Terminal works with **any NIP-07 signer** (nos2x, Alby, etc.), but RDWE Signer unlocks every feature:

- ✅ Full **NIP-04** + **NIP-44** support (most signers only ship one)
- ✅ Zero external dependencies — every line of crypto is auditable
- ✅ Per-site permission system with "Always allow" memory
- ✅ AES-256-GCM nsec encryption with PBKDF2 (310k iterations)
- ✅ Built specifically for the RDWE ecosystem
- ✅ 16 RFC-grade crypto self-tests run on every boot

**Without RDWE Signer, you may miss out on:**
- NIP-17 gift-wrapped DMs (most modern privacy DMs)
- NIP-44 modern encryption (legacy NIP-04 only)
- Cross-client conversation key consistency

---

## 📚 Full Installation Guide

### Step 1: Install a NIP-07 Signer

**The Recommended Path:**
1. Download [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)
2. Load as unpacked extension in Chrome/Brave/Edge
3. Generate or import your `nsec`
4. Set a master password
5. You're done

**Alternative Signers:**
- [nos2x](https://github.com/fiatjaf/nos2x) (Chrome/Firefox)
- [Alby](https://getalby.com/) (Chrome/Firefox/Safari)
- [Flamingo](https://www.getflamingo.org/) (Chrome)

### Step 2: Open the Terminal

Just open `index.html`. The header bar will detect your signer and show your `npub`.

### Step 3: Load Your Feed

Click **⚡ MY FEED** to load your timeline.

Or paste any `npub1...` into the search bar to view someone's profile.

### Step 4: Configure Your Relays (Optional)

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
The terminal also reads your NIP-65 relay list from your signer automatically.

---

## ✅ Post-Installation Verification

After installation, verify everything works:

### 1. Check Signer Detection

Open the terminal — the header bar should show:
- ✅ Your `npub` (truncated)
- ✅ Green "NIP-07" indicator
- ✅ "NIP-04" and "NIP-44" badges (if signer supports them)

### 2. Check Relay Connections

Look at the top of the page — you should see:
- ✅ `RELAYS: X/Y` (X connected, Y total)
- ✅ Green dots next to each connected relay

### 3. Test Feed Loading

1. Click **⚡ MY FEED**
2. Notes should appear within 2-5 seconds
3. Avatars and names should load progressively

### 4. Test Composing

1. Click **✍ COMPOSE**
2. Type a test note: `🐉 Testing RDWE Nostr Terminal v3.2.3`
3. Click "POST"
4. Your signer should prompt for permission
5. Approve → note appears in your feed within seconds

### 5. Test DMs (if you have conversations)

1. Click **📨 DMS**
2. Existing conversations should appear in sidebar
3. Click a conversation → messages decrypt and display

---

## 🎮 Usage

### Tab Overview

| Tab | What It Does |
| --- | --- |
| **📡 FEED** | Your follow-graph timeline |
| **🌐 GLOBAL** | The entire Nostr firehose (live) |
| **👤 PROFILE** | View any user's profile by npub |
| **🧵 THREADS** | Threaded conversations (NIP-10) |
| **🔔 NOTIFS** | Likes, reposts, mentions, zaps |
| **✍ COMPOSE** | Markdown editor with hashtag autocomplete |
| **🔍 SEARCH** | NIP-50 server-side search |
| **👥 FOLLOWING** | Your follow list |
| **👥 FOLLOWERS** | People who follow you |
| **📨 DMS** | Encrypted DMs (NIP-04/44/17) |
| **⚡ ZAPS** | Zap inbox + send zaps |
| **🔖 BOOKMARKS** | Encrypted bookmarks (NIP-51) |
| **🔇 MUTES** | Mute people + hashtags (NIP-51) |
| **💻 TERMINAL** | Raw event firehose (developer view) |
| **📶 RELAYS** | Manage relays + NIP-11 info |
| **🔐 NIP-05** | Generate `nostr.json` for your domain |
| **⚙ SETTINGS** | Encryption preferences, autoplay, sensitive content |

### Power User Tips

**Quote a note:** Click the 🔗 link icon, then "QUOTE" in compose.

**Zap with custom amount:** Click ⚡ on any note, edit amount in modal.

**Search by hashtag:** Type `#bitcoin` in search.

**Search by note ID:** Paste any `note1...` or `nevent1...` in search.

**Find your conversations fast:** DM search filters by name or npub.

---

## 🔧 Configuration

The terminal stores all settings in `localStorage` — nothing leaves your browser.

### Settings You Can Change

- **Default Encryption** — NIP-04 (legacy) or NIP-44 (modern)
- **Autoplay Media** — Auto-play videos in feed (off by default)
- **Sensitive Content** — Show/hide NIP-36 marked content
- **Hide Muted** — Hide notes from muted users

### Want Different Default Relays?

Find `DEFAULT_RELAYS` in the script block and edit the array:

```javascript
const DEFAULT_RELAYS = [
  'wss://your-relay.com',
  'wss://another-relay.io',
  // ...
];
```

### Want to Customize the Look?

CSS variables are at the top of the `<style>` block:

```css
:root {
  --bg: #000;            /* background */
  --red: #ff0000;        /* primary accent */
  --green: #00ff00;      /* secondary accent */
  --cyan: #00ccff;       /* links */
  --yellow: #ffcc00;     /* zaps */
  --purple: #aa44ff;     /* mentions */
  /* ... */
}
```

It's one file. Read it, fork it, ship it.

---

## 🐛 Troubleshooting

### "No signer detected"

**Fix:**
- Make sure your NIP-07 extension (RDWE Signer, nos2x, Alby, etc.) is installed and unlocked
- Reload the page after installing the signer
- Some signers require granting permission per site — check the signer's UI

### "Relays disconnected" or stuck connecting

**Fix:**
- Check your internet connection
- Some networks block WebSocket connections — try a different network
- Go to **📶 RELAYS** tab and remove unreachable relays
- Add known-good relays: `wss://nos.lol`, `wss://relay.damus.io`

### "Profile won't load" or avatars missing

**Fix:**
- Profile load can take 5-10 seconds on slow relays
- Some users have profiles only on specific relays — try adding `wss://relay.nostr.band` (search-friendly)
- Avatars use lazy loading — scroll near them to trigger load

### "Can't decrypt this DM"

**Fix:**
- The DM might be NIP-44 but your signer only supports NIP-04 (or vice versa)
- Use [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer) which supports both
- NIP-17 gift-wrapped DMs require NIP-44 support

### "Zap button doesn't open wallet"

**Fix:**
- Make sure your wallet supports `lightning:` URIs (most do)
- The terminal opens the wallet via `window.open()` — popup blockers may interfere
- Use the **COPY** button if `window.open()` fails — paste the invoice into your wallet

### "Compose post stuck on 'PUBLISHING...'"

**Fix:**
- Some relays reject posts due to AUTH requirements (NIP-42) — check the **💻 TERMINAL** tab for rejection messages
- Posts publish to multiple relays — even if some fail, others usually succeed
- Wait 5-10 seconds — the timeout is generous

### "Underscores in my repo names get mangled"

**Fixed in v3.2.3!** Update to the latest version. Underscores inside words like `RDWE_Nostr_Terminal` now render correctly.

### Performance issues with large feeds

**Fix:**
- The terminal uses virtual scrolling — only visible notes render
- If lag persists, lower **Global firehose** activity in the GLOBAL tab
- Clear browser cache and reload

---

## 🔐 Security Best Practices

### Your nsec Never Touches the App

This terminal **never asks for your private key**. All signing happens via NIP-07.

### Use HTTPS in Production

If you host the terminal on your own server, **use HTTPS**. The terminal connects to `wss://` relays (encrypted) but page-level HTTPS adds another layer.

### Verify Your Signer

Before using any signer, audit its source code or use a known-good one.
[RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer) has zero dependencies — every line is auditable.

### Don't Paste nsec Anywhere

Not into the terminal. Not into any website. Not into a "magic Nostr login" page.
A legit Nostr client **never** asks for your `nsec`.

---

## 🔧 Technical Details

### Stack

**Pure Vanilla JavaScript:**
- No React, no Vue, no Svelte
- No Tailwind, no Bootstrap
- No webpack, no vite, no build step
- No npm, no node_modules, no package.json

**Browser APIs Only:**
- WebSocket (relay connections)
- Web Crypto API (signature verification)
- IntersectionObserver (lazy loading)
- MutationObserver (auto-attach observers)
- localStorage (settings + cache)
- requestAnimationFrame (render throttle)

**Single File Architecture:**
- `index.html` contains:
  - HTML structure
  - All CSS (in `<style>` block)
  - All JavaScript (in `<script>` block)
  - SVG icons (inline)
  - Favicon (inline data URI)

### How It Works

1. **Boot Sequence:**
   - Detects NIP-07 signer
   - Fetches user's pubkey
   - Connects to default + NIP-65 relays
   - Subscribes to user's contacts (kind 3)
   - Starts global firehose monitor

2. **Feed Rendering:**
   - Subscribes to authors' notes (kind 1)
   - Notes arrive via WebSocket
   - Virtual scroll renders only visible notes (~30 at a time)
   - Avatars + reactions lazy-load via IntersectionObserver

3. **Profile Lookups:**
   - Batched fetches (80ms debounce, 200 pubkeys per batch)
   - LRU cache (max 1000 profiles)
   - Auto-update rendered cards via MutationObserver

4. **DM Handling:**
   - NIP-04 decrypts via signer's `nip04.decrypt`
   - NIP-44 decrypts via signer's `nip44.decrypt`
   - NIP-17 unwraps gift-wrap → seal → real DM
   - Auto-detects encryption per message

### Performance Benchmarks

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

### Lazy Loading Architecture

- **Virtual scrolling** on Feed/Global/Search/Bookmarks/Zaps/Notifs (20-30 chunks)
- **IntersectionObserver** for images (load when 400px from viewport)
- **Lazy reaction fetch** — only subscribes for visible notes
- **Profile LRU cache** — max 1000 entries, oldest evicted automatically
- **rAF render throttle** — handles firehose without UI thrash
- **MutationObserver safety net** — auto-attaches observers to any new DOM node

---

## 📋 NIP Coverage

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
| NIP-19 | Bech32 entities (with TLV) | ✅ Full |
| NIP-21 | `nostr:` URI scheme | ✅ Clickable |
| NIP-23 | Long-form articles | ✅ Read + Publish |
| NIP-25 | Reactions + custom emoji | ✅ Full |
| NIP-27 | Text note references | ✅ Full |
| NIP-30 | Custom emoji | ✅ Display |
| NIP-36 | Sensitive content (CW) | ✅ Display + Publish |
| NIP-42 | Relay AUTH | ✅ Auto-handles |
| NIP-44 | Modern encryption (ChaCha20) | ✅ Full |
| NIP-50 | Search capability | ✅ Auto-detects |
| NIP-51 | Mute lists & bookmarks | ✅ Public + encrypted |
| NIP-56 | Reporting | ✅ Full |
| NIP-57 | Lightning Zaps | ✅ Full LNURL flow |
| NIP-65 | Relay list (outbox model) | ✅ Routes by author |
| NIP-89 | Client identification | ✅ Tagged |
| NIP-92 | Media attachments (imeta) | ✅ Parse + emit |

---

## 📈 Changelog

### v3.2.3 (Current) — Underscore Fix

- 📝 **Intra-word underscore fix** — `RDWE_Nostr_Terminal` and other snake_case text no longer mangled by italic markdown
- Follows CommonMark spec: underscores inside words don't trigger italic
- Normal `_italic_` still works
- 9/9 regex tests pass

### v3.2.2 — URL Fix + Version Centralization

- 🔗 Underscores in URLs no longer eaten by italic markdown
- 🔢 Centralized version display via `data-version` + `updateVersionStrings()`
- Bump `CLIENT_VERSION` once, all 12 UI elements auto-update

### v3.2.1 — Avatar Bugfix

- 🖼 Lazy avatars upgrade in-place when profile arrives
- 📛 Display names auto-update across all rendered cards via `data-pk-name`
- 👁 Global MutationObserver auto-attaches lazy observers to any new DOM node

### v3.2 — Performance Beast

- 🚀 Virtual scrolling on Feed/Global/Search/Bookmarks/Zaps/Notifs
- 🖼 IntersectionObserver image lazy-load
- ⚡ Lazy reaction fetch (only visible notes)
- 📨 DM pagination (last 50, scroll-up loads older)
- ⏱ rAF render throttle on every render function
- 💾 Profile LRU cache (max 1000)
- 📺 Terminal batch flush via DocumentFragment

### v3.1 — Daily Driver

- ⚡ Zaps with QR codes + COPY + window.open()
- 📨 Full DM stack (NIP-04 + NIP-44 + NIP-17)
- 📱 Mobile responsive (34px+ touch targets, master/detail nav)
- 🎬 Lazy media load (max 2 videos auto)
- 🔧 Modal class unified to `.open`

---

## 🌐 Compatible Signers

Any NIP-07 browser extension will work:

- ⭐ **[RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)** *(recommended — full NIP-04 + NIP-44 + audited zero-dep crypto)*
- [nos2x](https://github.com/fiatjaf/nos2x)
- [Alby](https://getalby.com/)
- [Flamingo](https://www.getflamingo.org/)
- [Nostore](https://apps.apple.com/us/app/nostore/id1666553677) (iOS)
- [Amber](https://github.com/greenart7c3/Amber) (Android, via NIP-46 bridge)

---

## 🤝 Contributing

We welcome contributions! Here's how:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

### Contribution Guidelines

- ✅ Keep it **single-file**
- ✅ Keep it **zero dependencies**
- ✅ Keep it **build-step-free**
- ✅ Compatible with offline `file://` use
- ✅ Follow existing code style
- ✅ Test on a live Nostr account before PR
- ❌ No npm packages
- ❌ No frameworks
- ❌ No CDN imports (except optional Google Fonts)
- ❌ No telemetry, no tracking, no phone-home
- ❌ Don't change the license

If you can't fit it in `index.html`, it doesn't belong in this project.

---

## 📜 License

**RDE Black Flag Source License v6.66**

```
###################################################################################
#                                                                                 #
#      .:: RED DRAGON ELITE (RDE)  -  BLACK FLAG SOURCE LICENSE v6.66 ::.         #
#                                                                                 #
#   PROJECT:    RDWE_NOSTR_TERMINAL (STANDALONE NOSTR WEB CLIENT)                 #
#   ARCHITECT:  .:: RDE ⧌ Shin [△ ᛋᛅᚱᛒᛅᚾᛏᛋ ᛒᛁᛏᛅ ▽] ::. | https://rd-elite.com     #
#   ORIGIN:     https://github.com/RedDragonElite                                 #
#                                                                                 #
#   WARNING: THIS CODE IS PROTECTED BY DIGITAL VOODOO AND PURE HATRED FOR LEAKERS #
#                                                                                 #
#   [ THE RULES OF THE GAME ]                                                     #
#                                                                                 #
#   1. // THE "FUCK GREED" PROTOCOL (FREE USE)                                    #
#      You are free to use, edit, host, and abuse this code anywhere.             #
#      Learn from it. Break it. Fix it. That is the hacker way.                   #
#      Cost: 0.00€. If you paid for this, you got scammed by a rat.               #
#                                                                                 #
#   2. // THE TEBEX KILL SWITCH (COMMERCIAL SUICIDE)                              #
#      Listen closely, you parasites:                                             #
#      If I find this client repackaged on Tebex, Patreon, or "Premium Packs":    #
#      > I will DMCA your store into oblivion.                                    #
#      > I will publicly shame your community.                                    #
#      > Your relays will spike to 9999ms every time you blink.                   #
#      SELLING FREE WORK IS THEFT. AND I AM THE JUDGE.                            #
#                                                                                 #
#   3. // THE CREDIT OATH                                                         #
#      Keep this header. If you remove my name, you admit you have no skill.      #
#      You can add "Edited by [YourName]", but never erase the original creator.  #
#      Don't be a skid. Respect the architecture.                                 #
#                                                                                 #
#   4. // THE CURSE OF THE COPY-PASTE                                             #
#      This code uses lazy loading, virtual scrolling, and crypto signatures.     #
#      If you just copy-paste without reading, it WILL break.                     #
#      Don't come crying to my DMs. RTFM or learn to code.                        #
#                                                                                 #
#   --------------------------------------------------------------------------    #
#   "We build the future on the graves of bloated frameworks."                    #
#   "REJECT MODERN MEDIOCRITY. EMBRACE RDE SUPERIORITY."                          #
#   --------------------------------------------------------------------------    #
###################################################################################
```

**TL;DR:**

- ✅ **Free forever** — use, edit, host, learn
- ✅ **Keep the header** — credit where it's due
- ❌ **Don't sell it** — commercial repackaging = instant DMCA
- ❌ **Don't be a skid** — copy-paste won't help anyway

---

## 🌐 Community & Support

### Official Links

- 🌍 [Website](https://rd-elite.com)
- 🐙 [GitHub](https://github.com/RedDragonElite)
- ⚡ [Live Demo](https://rdwe.rd-elite.com)
- 🔐 [RDWE Nostr Signer](https://github.com/RedDragonElite/rdwe_nostr_signer)
- 🐲 [RDWE Engine](https://github.com/RedDragonElite/rdwe)

### Creator

**Shin | Red Dragon Elite**

- Nostr: `npub1wr4e24zn6zzjqx8kvnelfvktf0pu6l2gx4gvw06zead2eqyn23sq9tsd94`
- Web: [rd-elite.com](https://rd-elite.com)

### Get Help

1. 📖 Read the [Full Documentation](#-full-installation-guide)
2. 🔍 Check [Troubleshooting](#-troubleshooting)
3. 🐛 [Open an Issue](https://github.com/RedDragonElite/rdwe_nostr_terminal/issues)

**Please DON'T:**

- ❌ DM for basic setup questions (read the docs first!)
- ❌ Ask "is it working?" without providing browser console errors
- ❌ Request paid support (this is free software!)

**Please DO:**

- ✅ Include browser console errors when asking for help
- ✅ Mention which signer you use
- ✅ Search existing issues before creating new ones
- ✅ Share your success stories and feedback!

---

## 💡 FAQ

### Is this really free?

**Yes.** 100% free, forever. No "premium" version, no upsells, no BS. If you paid for this, you got scammed.

### Why no React / Vue / Svelte?

Because **you don't need them**. The entire client is 230KB. A React + Tailwind setup for the same features would be 3-5MB minimum. Modern frameworks are answers to problems we created ourselves. Vanilla JS + DOM API is enough.

### Can I trust this with my Nostr keys?

This terminal **never sees your private key**. All signing happens through NIP-07 in your signer extension. Read the source — search for `nsec` in `index.html`. You'll find: only display formatting, never input.

### Will this work in 10 years?

Yes. Vanilla JS + browser APIs are stable for decades. No `npm install` to break, no framework upgrades to crash, no CDN dependencies to disappear. Open the file in 2035 — it'll still work.

### Why no theme switching / light mode?

The cyberpunk red-on-black aesthetic is opinionated by design. CSS variables are exposed at the top of the `<style>` block — fork it and theme it however you want. PRs for additional themes welcome.

### Can I use this on mobile?

Yes! Fully responsive. Touch targets are 34px+. Mobile Safari and Chrome both work great. Add to home screen for app-like experience.

### What about offline use?

Once `index.html` is loaded, it works offline for everything except relay communication (which obviously needs internet). Future v3.3+ may add Service Worker for true offline mode.

### Why no notifications API / push?

Privacy. Push notifications require a server intermediary that sees who you talk to. The terminal stays 100% client-side. Open it in a tab, leave it running — that's your "notification system".

### Can I build my own client on top of this?

**Yes please!** Fork it, strip what you don't need, add what you want. Just keep the BFS license header. Build the next great Nostr client.

### Why "RDWE"?

**R**ed **D**ragon **W**eb **E**ngine. The PHP framework this terminal was originally built for. The terminal works standalone — RDWE engine is optional.

### Is there a desktop app?

Not yet. But you can wrap `index.html` in Electron, Tauri, or Wails in 5 minutes if you want. PRs for a Tauri build configuration welcome.

### Does this work with relay AUTH (NIP-42)?

Yes — auto-handles AUTH challenges via your NIP-07 signer. Compatible with paid relays (relay.damus.io paid tier, etc.).

### Can I use Tor / VPN?

Yes — it's just WebSocket over HTTPS. Use any privacy tooling that handles `wss://` connections. Relay diversity protects against single-relay surveillance.

### How big is the production traffic footprint?

Per page-load: ~230KB (HTML+CSS+JS) + lazy-loaded media. After load: only WebSocket relay traffic + image fetches when scrolling. **No** Google Analytics, **no** tracking pixels, **no** A/B test scripts.

---

## 🏆 Credits

**Built by:** [Red Dragon Elite](https://rd-elite.com)
**Creator:** Shin

**Special Thanks:**

- The Nostr protocol designers (fiatjaf and contributors)
- Every NIP author for keeping the protocol open
- The open-source community that proved frameworks aren't necessary
- Everyone who believes in decentralization
- The early testers who reported bugs and made v3.2.3 possible

---

## ⚡ One More Thing...

**If you like this project:**

- ⭐ **Star this repo** (helps others discover it!)
- 🍴 **Fork it** (build something cool!)
- 💬 **Share it** (spread the word!)
- 🐉 **Follow us** on Nostr

**Remember:**

> "We build the future on the graves of bloated frameworks."
> — Red Dragon Elite

---

**Made with 🔥 by [Red Dragon Elite](https://rd-elite.com)**

*REJECT MODERN MEDIOCRITY. EMBRACE RDE SUPERIORITY.*

[![Website](https://img.shields.io/badge/Website-Visit-red?style=for-the-badge&logo=google-chrome)](https://rd-elite.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/RedDragonElite)
[![Nostr](https://img.shields.io/badge/Nostr-Follow-purple?style=for-the-badge&logo=rss)](https://primal.net/p/npub1wr4e24zn6zzjqx8kvnelfvktf0pu6l2gx4gvw06zead2eqyn23sq9tsd94)

⚡ **777** ⚡ FREEDOM > CONTROL · QUALITY > PROFIT · COMMUNITY > CORPORATION ⚡ **777** ⚡
