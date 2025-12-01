# 🎮 DEV-MAN: A Developer's Nightmare

An incredibly polished, viral-worthy Pac-Man style game for your GitHub profile!

## ✨ New! Interactive README Features

Your README now includes several interactive elements that display **directly on your profile page**:

### 1. 🌊 Animated Header & Footer
- Beautiful gradient waves that animate on page load
- Customized with your name and title

### 2. ⌨️ Typing Animation  
- Dynamic text that types out different messages
- Powered by [readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg)

### 3. 🎮 DEV-MAN Animated Banner
- Custom SVG animation showing the game in action
- Clickable to play the full game

### 4. 🐍 Contribution Snake Animation
**Requires GitHub Action setup** (see below):
- A snake that "eats" your GitHub contribution graph
- Updates automatically every day

### 5. 📊 Enhanced Stats
- GitHub stats with custom theming
- Streak stats
- Activity graph
- GitHub trophies

---

## 🐍 Setting Up the Contribution Snake

The snake animation requires a GitHub Action to generate daily. Here's how to set it up:

1. **Create the workflow file** at `.github/workflows/snake.yml` (already included)

2. **Push to your profile repository** (`pc9350/pc9350`)

3. **Run the action manually the first time:**
   - Go to your repo on GitHub
   - Click "Actions" tab
   - Select "Generate Snake Animation"
   - Click "Run workflow"

4. **The snake SVG will be available at:**
   ```
   https://raw.githubusercontent.com/pc9350/pc9350/output/github-snake.svg
   https://raw.githubusercontent.com/pc9350/pc9350/output/github-snake-dark.svg
   ```

---

## 🚀 Quick Start

### Option 1: GitHub Pages Deployment (Recommended)

1. **Create a new repository** named `dev-man` (or add to existing repo)

2. **Upload the `dev-man.html` file** to the repository

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Choose `main` branch and `/ (root)` folder
   - Click Save

4. **Access your game at:**
   ```
   https://pc9350.github.io/dev-man/dev-man.html
   ```

### Option 2: Add to Profile Repository

If you have a `pc9350/pc9350` profile repository:

1. Create a `games/` folder in your profile repo
2. Upload `dev-man.html` to `games/`
3. Enable GitHub Pages on your profile repo
4. Access at: `https://pc9350.github.io/pc9350/games/dev-man.html`

---

## 📝 README Integration

### Hero Section (Maximum Impact)

Add this right after your name/title in your profile README:

```markdown
## 🎮 Play DEV-MAN: A Developer's Nightmare

<div align="center">
  <a href="https://pc9350.github.io/dev-man/dev-man.html">
    <img src="https://img.shields.io/badge/🕹️_PLAY_NOW-DEV--MAN-00ff88?style=for-the-badge&labelColor=0a0a0f" alt="Play DEV-MAN"/>
  </a>
  <br><br>
  <a href="https://pc9350.github.io/dev-man/dev-man.html">
    <img src="game-preview.gif" alt="DEV-MAN Game Preview" width="500"/>
  </a>
  <br>
  <sub>🐛 Dodge bugs • ⚠️ Escape merge conflicts • ☕ Power up with coffee!</sub>
</div>

> **Challenge:** Can you clear all the code and survive the tech debt? 🏆

---
```

### Compact Version

```markdown
### 🎮 Take a Break!

[![Play DEV-MAN](https://img.shields.io/badge/🕹️_Play-DEV--MAN-00ff88?style=flat-square&labelColor=0a0a0f)](https://pc9350.github.io/dev-man/dev-man.html)
A developer-themed Pac-Man game I built! Dodge bugs, escape merge conflicts, and power up with coffee ☕
```

### With Stats Badge

```markdown
## 🎮 DEV-MAN

<div align="center">

[![Play Now](https://img.shields.io/badge/▶_PLAY_NOW-00ff88?style=for-the-badge&logo=github&logoColor=white)](https://pc9350.github.io/dev-man/dev-man.html)
[![Made With](https://img.shields.io/badge/Made_With-Pure_JavaScript-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)](https://pc9350.github.io/dev-man/dev-man.html)
[![Lines of Code](https://img.shields.io/badge/Lines_of_Code-1000+-blue?style=for-the-badge)](https://pc9350.github.io/dev-man/dev-man.html)

**A Pac-Man clone built entirely in vanilla JavaScript with:**
- 🐛 Smart enemy AI using A* pathfinding
- 🎨 Neon cyberpunk visuals
- 📱 Mobile-responsive with touch controls
- 🏆 Achievement system & high scores
- 🔊 Procedurally generated sound effects

</div>
```

---

## 🎯 Game Features

### Gameplay Elements

| Element | Description | Points |
|---------|-------------|--------|
| `·` Dots | Collect all to win | 10 pts |
| ☕ Coffee | Power-up - makes enemies vulnerable | 50 pts |
| ⭐ Stars | Bonus collectibles | 50 pts |
| 🐛 Bug | Aggressive enemy - chases directly | 200 pts (when scared) |
| ⚠️ Merge Conflict | Ambush enemy - predicts your path | 200 pts (when scared) |
| 💀 Tech Debt | Random enemy - unpredictable | 200 pts (when scared) |

### Controls

| Platform | Controls |
|----------|----------|
| Desktop | Arrow keys or WASD to move, P to pause, R to restart, M for sound |
| Mobile | Swipe or use on-screen D-pad |

### Easter Eggs 🥚

- **Konami Code:** ↑↑↓↓←→←→BA - Unlocks 99 lives!
- **Achievement System:** Unlock badges for various accomplishments
- **Combo System:** Collect items quickly for score multipliers

---

## 🛠️ Customization

### Colors

Edit the CSS variables at the top of the file:

```css
:root {
    --neon-green: #00ff88;    /* Primary accent */
    --neon-blue: #00d4ff;     /* Secondary accent */
    --neon-pink: #ff00ff;     /* Highlights */
    --neon-yellow: #ffff00;   /* Player color */
    --bg-dark: #0a0a0f;       /* Background */
}
```

### Difficulty

Modify the `CONFIG` object in JavaScript:

```javascript
const CONFIG = {
    PLAYER_SPEED: 4,          // Increase for easier
    ENEMY_SPEED: 3,           // Decrease for easier
    POWER_UP_DURATION: 5000,  // Milliseconds
    INITIAL_LIVES: 3,         // Starting lives
};
```

### Maze Layout

The maze is defined in `BASE_MAZE` array:
- `0` = Wall
- `1` = Dot
- `2` = Empty path
- `3` = Power pellet (Coffee)
- `4` = Ghost house
- `5` = Ghost house gate

---

## 📱 Browser Compatibility

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ✅ Full |

---

## 🎨 Creating a Preview GIF

To create an eye-catching preview GIF for your README:

### Using ScreenToGif (Windows)
1. Download [ScreenToGif](https://www.screentogif.com/)
2. Record ~10 seconds of gameplay
3. Export as GIF (max 5MB for GitHub)

### Using Kap (macOS)
1. Download [Kap](https://getkap.co/)
2. Record gameplay
3. Export as GIF

### Recommended GIF Settings
- **Duration:** 5-10 seconds
- **Resolution:** 500-600px width
- **Frame rate:** 15-20 fps
- **File size:** Under 5MB

---

## 🏆 Achievements

| Achievement | Requirement | Badge |
|-------------|-------------|-------|
| Coffee Addict | Grab your first coffee | ☕ |
| Bug Hunter | Eat all 3 enemies in one power-up | 🐛 |
| Star Collector | Collect a GitHub star | ⭐ |
| Build Successful | Complete a level | ✅ |
| Konami Master | Enter the Konami code | 🎮 |

---

## 🔧 Technical Details

### Architecture
- **Pure Vanilla JavaScript** - No dependencies
- **HTML5 Canvas** - 60fps rendering
- **Web Audio API** - Procedural sound generation
- **localStorage** - High score persistence

### AI System
- **A* Pathfinding** - Efficient enemy navigation
- **Behavior Patterns:**
  - Bug: Direct chase (Blinky-style)
  - Merge Conflict: Predictive ambush (Pinky-style)
  - Tech Debt: Random/Erratic (Clyde-style)

### Performance
- Optimized canvas rendering
- Efficient collision detection
- Smooth 60fps on all devices
- Minimal memory footprint

---

## 📄 License

MIT License - Feel free to modify and share!

---

## 🙏 Credits

Created by [Pranav Chhabra](https://github.com/pc9350)

Inspired by the classic Pac-Man game by Namco

---

<div align="center">
  <b>If you enjoyed this game, consider giving it a ⭐!</b>
</div>

