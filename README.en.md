<div align="center">

# 🌸 CardChat (藏春阁)

**An AI character roleplay platform that speaks the whole Tavern ecosystem**

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md)

Live demo → **https://ccg.officechat.com.cn**

</div>

---

<p align="center">
  <img src="docs/images/chat.jpg" alt="Chat" width="49%">
  <img src="docs/images/discover.jpg" alt="Discover" width="49%">
</p>

CardChat is a complete AI character chat platform: character cards, world books, presets, long-term memory,
group chat, image generation, subscriptions, billing and an admin console — ready to run.
It does more than chat: it brings the whole SillyTavern-style ecosystem to the web, with less friction.

---

## 1. Full Tavern ecosystem support

**SillyTavern cards (v1 / v2)**, **Chub.ai** and **JanitorAI** formats are all supported — PNG and JSON cards import
directly, keeping the persona, first message, example dialogue and embedded world book intact.

<p align="center">
  <img src="docs/images/characters.jpg" alt="Character management" width="72%">
</p>

**Cards can be read and edited directly.** No format conversion, no re-typing — open a card and change the persona,
the greeting, the avatar or the tags.

<p align="center">
  <img src="docs/images/character.jpg" alt="Character detail" width="72%">
</p>

## 2. One-click card generation

Don't feel like writing a persona? Describe the character in one sentence and the AI fills in the name, description,
personality, greeting and tags. Pick a style (romance / fantasy / campus / workplace / mystery / healing…) and refine
afterwards.

<p align="center">
  <img src="docs/images/create.jpg" alt="One-click card generation" width="72%">
</p>

## 3. Single chat and group chat

**Single chat**: streaming replies, multiple branches (swipe), regenerate, edit and resend, quoted replies, export.

<p align="center">
  <img src="docs/images/chat.jpg" alt="Single chat" width="72%">
</p>

**Group chat**: put several characters in one conversation, `@`-mention who should speak, and only that character
answers. Characters also pick up on each other — an ensemble feel single chat can't give you.

<p align="center">
  <img src="docs/images/chat-group.jpg" alt="Group chat" width="72%">
</p>

## 4. Images and web search

- Send images; multimodal models can see and talk about them
- Web search results are merged into context when real-time information is needed
- Image / video generation is integrated and **currently in testing**

## 5. One-click jailbreak preset import

Jailbreaking used to mean hand-assembling prompts and tuning parameters. Now import a SillyTavern preset JSON —
entries are split, toggled individually, and can be bound per conversation.

<p align="center">
  <img src="docs/images/presets.jpg" alt="Presets" width="72%">
</p>

Presets also expose **Temperature, Top P, Top K, Min P, Frequency / Presence / Repetition Penalty** and more, so
**model parameters are fully user-configurable** without touching code.

## 6. World books

Three layers: global, character-embedded and per-conversation. Import SillyTavern world books, edit entries by hand,
and trigger them by keyword.

<p align="center">
  <img src="docs/images/worldbook.jpg" alt="World books" width="72%">
</p>

## 7. User personas and settings

Everyone gets a persona: avatar, nickname, personality, description. Switch any time — characters talk to *your*
persona instead of a generic "user".

<p align="center">
  <img src="docs/images/profile.jpg" alt="Profile" width="49%">
  <img src="docs/images/settings.jpg" alt="Settings" width="49%">
</p>

Settings let you choose the **platform API** (coins, billed at list price) or plug in **your own API key** (no coins),
with your own base URL and model.

## 8. Rewards

- **Daily check-in** — fixed coins, once a day
- **Creation rewards** — publish a card to earn, plus bonuses for likes and downloads
- **Invites** — invite-code signup rewards both sides
- **First-purchase offers / subscription plans** — two paths to top up

<p align="center">
  <img src="docs/images/subscription.jpg" alt="Subscription" width="72%">
</p>

---

## More features

| Feature | Description |
|---|---|
| Discover & recommendations | Pick tags (romance / healing / workplace / fantasy / horror…), then swipe through cards — like or skip, it learns |
| Long-term memory | Layered compression, fact extraction, hybrid retrieval — remembers you dozens of turns later |
| Auto messages | Characters message you on their own schedule |
| Leaderboards | Creators ranked by works, likes and usage |
| Notifications | Likes, comments, review results, announcements |
| Regex scripts | Display-layer replacement to remove AI tics and clean formatting |
| Export | Text or JSON |
| Follow creators | Keep up with an author's new works |
| i18n | Simplified Chinese, English, Japanese, Korean, French, Spanish |
| Mobile | Fully responsive, works in mobile browsers |

<p align="center">
  <img src="docs/images/discover-prefs.jpg" alt="Pick tags" width="24%">
  <img src="docs/images/discover-tags.jpg" alt="Tags selected" width="24%">
  <img src="docs/images/leaderboard.jpg" alt="Leaderboard" width="24%">
  <img src="docs/images/notifications.jpg" alt="Notifications" width="24%">
</p>

<p align="center">
  <img src="docs/images/chat-mobile.jpg" alt="Mobile chat" width="26%">
  <img src="docs/images/discover-mobile.jpg" alt="Mobile discover" width="26%">
  <img src="docs/images/auto.jpg" alt="Auto messages" width="26%">
</p>

---

## Admin console

Everything operational happens here: review, ban, adjust balances, inspect orders, change prices, publish
announcements, configure models.

<p align="center">
  <img src="docs/images/admin-dashboard.jpg" alt="Dashboard" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-users.jpg" alt="Users" width="49%">
  <img src="docs/images/admin-characters.jpg" alt="Card review" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-orders.jpg" alt="Orders" width="49%">
  <img src="docs/images/admin-ledger.jpg" alt="Coin ledger" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-platform.jpg" alt="Platform config" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-subscriptions.jpg" alt="Subscription plans" width="49%">
  <img src="docs/images/admin-comments.jpg" alt="Comment moderation" width="49%">
</p>

---

## Architecture

<p align="center">
  <img src="docs/architecture.svg" alt="Architecture" width="100%">
</p>

| Layer | Choice |
|---|---|
| Frontend | Vue 3 · TypeScript · Vite · SSE streaming |
| Backend | Node.js (22/24) · Express · TypeScript |
| Database | SQLite (WAL) · FTS5 full-text search |
| Model access | Any OpenAI-compatible gateway, streaming with non-streaming fallback |
| Deployment | Docker Compose · Nginx reverse proxy |

### How long-term memory works

The longer a chat runs, the more expensive context becomes. Memory is split into layers so a fixed token budget
buys the longest memory possible:

| Layer | What it does | Cost |
|---|---|---|
| **L1 working memory** | Slice the most recent raw messages by budget | Fixed per turn |
| **L2 chunk summaries** | One summary per 30 messages or 6,000 chars, never recomputed | Once per chunk |
| **L3 fact cards** | Identity / preference / relationship / event facts, deduplicated | With L2 |
| **Retrieval** | Keyword search against the current input, injected only on hits | One local query per turn |

Measured on real conversations: **~35% fewer prompt tokens**, while facts pushed out of the window are still
recalled correctly.

---

## Layout

```
.
├── README.md                 # Chinese (default)
├── README.en.md              # English
├── README.ja.md              # Japanese
├── docs/
│   ├── architecture.svg
│   └── images/
├── web/                      # frontend site, static-hostable
└── LICENSE
```

`web/` is a standard single-page app build. On Nginx, fall back unknown paths to `index.html`
(`try_files $uri /index.html`).

---

## License

**All Rights Reserved.** See [LICENSE](LICENSE).

<div align="center">
<sub>Made with 🌸</sub>
</div>
