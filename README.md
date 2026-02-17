# 🪨 📄 ✂️ Stone Paper Scissors - Mobile P2P

A modern, mobile-first Rock-Paper-Scissors game with real-time peer-to-peer multiplayer battles.

[🔴 Live Demo](https://samaed-samee.github.io/Stone-Paper-Scissors---Mobile-P2P/)


[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?logo=github)](https://github.com/samaed-samee)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-5-orange?logo=html5)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)

![Game Preview](./preview.png)

---

## ✨ Features

### 🎮 Game Modes
- **Local Mode** - Play against CPU with smart random selection
- **Online Mode** - Real-time P2P battles using 8-digit room codes

### 🎨 Beautiful UI/UX
- Glassmorphism design with backdrop blur effects
- Smooth animations (hand shake, winner reveal, spring effects)
- Particle effects on victory/defeat
- Full-screen flash feedback
- Mobile-optimized with safe-area support

### 🏆 Competitive Elements
- Real-time score tracking
- Round counter
- Instant visual feedback
- Toast notifications

---

## 🚀 Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic structure |
| **TailwindCSS** | Utility-first styling |
| **PeerJS** | WebRTC-based P2P connections |
| **Vanilla JavaScript** | Game logic & animations |
| **Google Fonts** | Plus Jakarta Sans typography |

---

## 🎯 How to Play

### Local Mode (vs CPU)
1. Select **Local** mode at the top
2. Tap **Stone 🪨**, **Paper 📄**, or **Scissors ✂️**
3. Watch the animated reveal
4. First to win rounds takes the lead!

### Online Mode (vs Rival)
1. Select **Online** mode
2. **Create Room** - Generate an 8-digit code and share it
3. **Join Room** - Enter your friend's 8-digit code
4. Both players select their moves
5. Real-time reveal determines the winner!

---

## 🌐 Online Multiplayer

The game uses **PeerJS** (WebRTC) for direct browser-to-browser connections:

```
Player 1 (Host)                    Player 2 (Joiner)
     │                                   │
     ├── Creates Room (8-digit code) ───┤
     │                                   │
     ├─── Sends move via P2P ───────────►│
     │◄──────── Sends move ──────────────┤
     │                                   │
     └────── Both reveal simultaneously ─┘
```

**No server required** - All game data transfers directly between players!

---

## 📦 Installation & Usage

### Option 1: Direct Play
Simply open `index.html` in any modern browser.

### Option 2: Local Server (Recommended)
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000`

### Option 3: Deploy to GitHub Pages
1. Push this repo to your GitHub
2. Go to **Settings > Pages**
3. Select your branch and save
4. Your game will be live at `https://yourusername.github.io/repo-name`

---

## 📁 Project Structure

```
Stone Paper Scissors/
├── index.html          # Main game file (all-in-one)
├── README.md           # This file
└── preview.png         # Game screenshot (add your own)
```

---

## 🎨 Animations & Effects

| Animation | Description |
|-----------|-------------|
| `hand-shake` | Rhythmic hand movement during countdown |
| `winner-pop` | Scale + glow effect for the winning hand |
| `loser-shrink` | Shrink + grayscale for the losing hand |
| `result-spring` | Bouncy text reveal for results |
| `particle-fly` | Confetti-like particles on win/lose |
| `flash-overlay` | Full-screen color flash on reveal |

---

## 📱 Mobile Optimization

- **Safe Area Support** - Respects notches and home indicators
- **Touch Optimized** - Large tap targets, haptic feedback
- **Responsive** - Adapts to all screen sizes
- **No Zoom** - Prevents accidental zoom on double-tap
- **Overscroll Disabled** - Prevents pull-to-refresh interference

---

## 🛠️ Customization

### Change Accent Colors
Edit CSS variables in `<style>`:
```css
:root {
    --accent-blue: #60a5fa;   /* Player color */
    --accent-rose: #fb7185;   /* Opponent color */
}
```

### Modify Game Speed
Adjust timeout values in `runReveal()`:
```javascript
await new Promise(r => setTimeout(r, 400)); // Countdown speed
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**samaed-samee**

[![GitHub](https://img.shields.io/badge/GitHub-@samaed--samee-black?logo=github)](https://github.com/samaed-samee)

---

## 🙏 Acknowledgments

- [TailwindCSS](https://tailwindcss.com/) - Utility-first CSS framework
- [PeerJS](https://peerjs.com/) - WebRTC abstraction library
- [Google Fonts](https://fonts.google.com/) - Plus Jakarta Sans typography
- [Emoji Kitchen](https://emojikitchen.dev/) - Emoji assets

---

<div align="center">

**Made with ❤️ by samaed-samee**

⭐ Star this repo if you enjoyed the game!

</div>
