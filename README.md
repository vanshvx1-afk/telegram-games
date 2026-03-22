# 🐱 Meow Games — BY VANSH

> **Premium Casino Games Web App** · Real Aviator-Style · Telegram Mini App · GitHub Pages Ready

<p align="center">
  <img src="https://i.ibb.co/JFqyY0BN/logo.png" width="100" style="border-radius:20px"/>
  <br/>
  <b>8 Games · Live Players · Admin Panel · VIP System · PWA</b>
</p>

---

## 📁 You Have 4 Versions

| Version | File | Notes |
|---------|------|-------|
| **v1** | `index.html (v1)` | Original release |
| **v2** | `index.html (v2)` | Improved UI + more games added |
| **v3** | `index.html (v3)` | Light theme + MeowFly redesign + bug fixes |
| **Latest** ✅ | `index.html` | **Always use this — most updated version** |

> 💡 **Always use the plain `index.html`** — it is the latest fully working version. The numbered versions are just backups.

### Which support files do you need?

| File | v1 | v2 | v3 | Latest |
|------|----|----|-----|--------|
| `index.html` | ✅ | ✅ | ✅ | ✅ |
| `sw.js` | ❌ | ❌ | ✅ | ✅ |
| `manifest.json` | ❌ | ❌ | ✅ optional | ✅ optional |

- **`sw.js`** — enables offline play and faster reload. Only available from v3 onwards.
- **`manifest.json`** — enables "Add to Home Screen" install prompt. Optional, game works without it.

> More versions will be added in the future. Same structure applies — just use the latest `index.html` + `sw.js`.

---

## 🚀 Deploy to GitHub Pages

**Step 1** — Upload these files to your repo root:
```
index.html
sw.js
manifest.json
README.md
```

**Step 2** — Enable GitHub Pages:
```
GitHub Repo → Settings → Pages → Source: main branch / root → Save
```

**Step 3** — Your game is live at:
```
https://yourusername.github.io/your-repo-name
```

### Run locally on your PC:
```cmd
cd your-folder
npx live-server
```
Or just open `index.html` directly in Chrome.

---

## 🎮 Games (8 Total)

| # | Game | Max Win | Description |
|---|------|---------|-------------|
| 1 | 💣 **Mines** | 24× | Find gems, avoid mines — cash out anytime to keep profit |
| 2 | 🐱 **Meow Fly** | ∞× | Aviator-style crash game — cash out before plane disappears |
| 3 | 🎲 **Dice** | 9.9× | Set a target number, roll below it to win |
| 4 | 🎡 **Wheel** | 5× | Spin the fortune wheel and land on a multiplier |
| 5 | ⚽ **Plinko** | 5× | Drop a ball through pegs — physics-based |
| 6 | 🃏 **Hi-Lo** | 12× | Guess if next card is higher or lower — chain wins for big multi |
| 7 | 🎱 **Keno** | 40× | Pick 1–10 numbers from 40, match as many as possible |
| 8 | 🎰 **Double Up** | 4× | Predict Red / Black or exact suit — streak multiplier |

> More games planned for future versions.

---

## ✏️ How to Edit

### 🔐 Admin Password
Search for `CFG.admin` in the file:
```js
admin: { pwd: 'vansh' }   // ← change to your password
```

### 🔊 Sounds
Search for `CFG.snd` — every game has its own sound block:
```js
mines: {
  safe:  'https://direct-url.mp3',   // gem found
  bomb:  'https://direct-url.mp3',   // mine hit
  win:   'https://direct-url.mp3',   // cashout win
  funny: 'https://direct-url.mp3',   // rare sound (7% chance)
  start: 'https://direct-url.mp3',   // game start
},
meowfly: {
  fly:     'https://direct-url.mp3', // plane takes off
  boom:    'https://direct-url.mp3', // crash
  cashout: 'https://direct-url.mp3', // cashout success
  loss:    'https://direct-url.mp3', // after crash
},
dice:  { roll, win, lose },
wheel: { spin, win, lose },
plinko:{ drop, bigwin, lose },
hilo:  { deal, win, lose, cash },
keno:  { pick, draw, hit, bigwin, lose }
```
Replace any URL string with a direct `.mp3` or `.wav` link from anywhere on the internet.

### 🎨 Dark Theme Colors
Search for `:root {`:
```css
:root {
  --pri:  #6c63ff;   /* purple — buttons, highlights */
  --suc:  #00e67a;   /* green — wins */
  --dan:  #ff4757;   /* red — losses, mines */
  --warn: #ffa502;   /* orange — warnings */
  --gold: #ffd700;   /* gold — VIP, achievements */
  --bg:   #080c18;   /* dark background */
}
```

### ☀️ Light Theme Colors
Search for `[data-theme="light"] {`:
```css
[data-theme="light"] {
  --pri: #5147e8;
  --bg:  #f0f2ff;
  /* edit any variable the same way */
}
```

### 📊 House Edge
Search for `edge:`:
```js
edge: 3,   // house edge % per game — 0 means no edge, 50 is max
```

### 📱 Telegram Bot Token
Search for `CFG.tg`:
```js
tg: {
  token: 'YOUR_BOT_TOKEN',   // from @BotFather
  admin: 'YOUR_CHAT_ID'      // your Telegram user ID
}
```

### 💰 Starting Balance
Search for `bal: 1000`:
```js
def: {
  bal: 1000,   // starting balance for new players
```

### 🎁 Daily Bonus Settings
Search for `CFG.bonus`:
```js
bonus: {
  min: 10,     // minimum bonus $
  max: 500,    // maximum bonus $
  cd:  864e5   // cooldown — 864e5 = 24 hours in milliseconds
}
```

### 🖼️ Logo / App Icon
Search for `i.ibb.co/JFqyY0BN/logo.png` and replace with your image URL.

### 👥 Fake Player Names
Search for `CFG.fakeNames`:
```js
fakeNames: ['Rahul S.', 'Priya K.', 'Arjun D.', ...]
// Add, remove or rename players shown in live feed and MeowFly
```

### 💬 Live Chat Messages
Search for `CFG.msgs` or `LiveChat.msgs`:
```js
msgs: ['🔥 lets gooo!', '💎 hit 3 gems!', ...]
// Edit or add messages that appear in the live chat
```

---

## 🛡️ Admin Panel

**How to open:** Tap the logo **5 times quickly** → enter password

**On desktop:** Press `Shift + A`

### 11 Tabs:

| Tab | What You Can Do |
|-----|----------------|
| 📊 **Stats** | Full session overview — balance, win rate, wagered, house P&L, player info |
| 🎛️ **Control** | Force win/lose, force N times, alternate, +$100 to +$1M, scenarios |
| 💣 **Mines** | See live mine map, reveal safe tile, trigger bomb, force cashout, refund bet |
| 🎮 **Games** | Monitor MeowFly multiplier live, force crash, HiLo card forcing |
| 🎰 **Rig** | Set exact dice result (1–100), crash point (×), wheel/plinko/keno win/lose |
| 👥 **Players** | Player profile, VIP level, loyalty points, add/remove fake players |
| 📈 **Analytics** | Win/loss bar chart, per-game P&L table, games/hour, export JSON & CSV |
| 🔔 **Alerts** | Toggle 7 notification types, set balance/streak/crash alert thresholds |
| 📨 **Telegram** | 10+ send buttons + 5 message templates (welcome, promo, VIP, etc.) |
| 📜 **Logs** | Full activity log with win/loss filter, export as .txt, send to TG |
| ⚙️ **Config** | House edge stepper, bonus controls, reset cooldown, system info |

### After Login — Extra Admin Features:
- 🔘 **Floating admin button** (bottom-right) — tap for instant panel access
- 🖱️ **Right-click button** — quick menu: +$1K, force win/lose, send report
- 🎬 **One-click scenarios** — Big Win, Bad Luck, Recovery, High Roller, Down to $10
- ⏸️ **Session control** — Pause all games, End all games

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `1` | Home |
| `2` | Mines |
| `3` | MeowFly |
| `4` | Dice |
| `5` | Wheel |
| `6` | Plinko |
| `7` | Hi-Lo |
| `8` | Keno |
| `9` | Dashboard |
| `0` | Leaderboard |
| `H` | History |
| `S` | Settings |
| `Space` | Cash out (in active game) |
| `Esc` | Close any overlay or popup |
| `?` | Show keyboard shortcuts help |
| `Shift + A` | Open admin panel |

---

## 📱 Mobile Features

- 👆 **Swipe left/right** to switch between screens
- 📲 **Install to home screen** like a native app (PWA)
- 📴 **Works offline** after first load via Service Worker
- 📳 **Haptic vibration** on taps, wins, and bombs
- 🌙 **Theme button** in header — switches light/dark instantly

---

## 🌟 All Special Features

| Feature | Description |
|---------|-------------|
| ⭐ **VIP System** | 6 levels: Bronze → Silver → Gold → Platinum → Diamond → Legend |
| 🎯 **Daily Missions** | 7 missions per day with $15–$75 coin rewards, auto-tracked |
| 🏅 **Achievements** | 10 unlockable badges with confetti animations |
| 🎡 **Daily Spin Wheel** | Free spin every 24h — 8 prize tiers up to $200 |
| 💬 **Live Chat** | Simulated player chat scrolling on home screen |
| 🏆 **Leaderboard** | Top 10 by profit, wins, streak, wagered |
| 🔥 **Win Streaks** | Streak tracker with banner animation |
| ♟️ **Bet Strategies** | Martingale, Fibonacci, D'Alembert for MeowFly |
| 🤖 **Auto-Play** | Mines auto-play mode with configurable round count |
| 🎱 **Keno Patterns** | Quick-select patterns: Corners, Diagonal, Cross, Top Row, Lucky 7s |
| 📊 **Win/Loss Analysis** | Avg win, avg loss, expected value, risk:reward ratio |
| 💹 **Crash Stats** | Live chart showing distribution of recent crashes |
| 🎆 **Fireworks** | On wins above $100 |
| ✨ **Gem Particles** | Sparkle burst when finding gems in Mines |
| 🛡️ **Bankroll Mode** | Auto-limit bets to max % of balance |
| 📤 **Share Results** | Share win card via Web Share API |
| 💾 **Auto-Save** | Every game result saved to localStorage instantly |
| 🌐 **Offline Play** | Service Worker caches everything |

---

## 🐱 MeowFly — Aviator Style

The main game — built to feel exactly like a real Aviator game:

- ✈️ Real SVG airplane with engine flame animation
- ⏱️ 2-second countdown timer before each round starts
- 👥 Live player bets bar — see other players cash out in real time
- 📈 Exponential multiplier curve drawn live on canvas with glow
- 💥 Red screen flash + plane crash animation on bust
- 🎯 Auto cashout at any multiplier you set
- 📊 Crash statistics — average, max, min, distribution chart
- 📜 Round history with sparkline SVG chart
- ♟️ Bet strategy engine — Martingale, Fibonacci, D'Alembert
- 🔔 Milestone alerts — pops toast at 2×, 5×, 10×, 20×, 50×, 100×
- 📁 Manual and Auto bet tabs

---

## 📂 File Structure

```
your-repo/
├── index.html        ← Complete game (single file, no dependencies)
├── sw.js             ← Service Worker (offline support + fast reload)
├── manifest.json     ← PWA config (install button, app icon, theme)
└── README.md         ← This file
```

The entire game runs from a **single `index.html` file** — no npm, no build step, no server required.

---

## 🐛 Troubleshooting

| Problem | Fix |
|---------|-----|
| JavaScript error on load | Download latest `index.html` — already fixed |
| `sw.js 404 error` | Put `sw.js` in same folder as `index.html` |
| `manifest.json 404` | Not critical — game works perfectly without it |
| Sounds not playing | Tap the screen once first — browser requires user interaction |
| Admin panel not opening | Tap the logo exactly 5 times quickly |
| Balance not saving | Make sure localStorage is not blocked in your browser |
| Game stuck after crash | Refresh the page — data is auto-saved |

---

## 🔮 Planned for Future Versions

- [ ] More crash game variants
- [ ] Slot machine
- [ ] Sports mini-game
- [ ] Custom avatar system
- [ ] Referral / invite rewards
- [ ] Real-time multiplayer rooms
- [ ] More admin rig controls
- [ ] Custom theme editor in admin

---

## 📞 Contact & Credits

| | |
|--|--|
| **Developer** | Vansh |
| **Telegram** | [@itsikiarai](https://t.me/itsikiarai) |
| **Stack** | Pure HTML + CSS + Vanilla JS — zero dependencies |
| **Hosting** | GitHub Pages (free) |

---

> ⚠️ **Entertainment purposes only.** This app uses fake virtual currency. No real money is involved at any point. Recommended for age 18+.
