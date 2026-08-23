<div align="center">

# 🐦 Flappy Bird — Python Clone

### A classic Flappy Bird recreation built with Python & Pygame

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
[![Pygame](https://img.shields.io/badge/Pygame-000000?style=for-the-badge&logo=python&logoColor=white)](https://img.shields.io/badge/Pygame-000000?style=for-the-badge&logo=python&logoColor=white)

</div>

---

## 📌 Description

A faithful clone of the classic **Flappy Bird** game, built entirely in Python using the Pygame library. Flap the bird through an endless series of pipes, rack up points for every pipe you clear, and try to beat your own high score — one wrong move and it's game over.

## 🎮 Controls

| Key | Action |
|---|---|
| `↑` / `Space` / `Enter` | Flap (bird rises) |
| Mouse Click | Flap (alternative to keyboard) |
| `P` / `Pause` | Pause / Resume |
| `Esc` | Quit |

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| 🐍 Python | Core game logic |
| 🎮 Pygame | Rendering, input, sound, and game loop |

## 📁 Project Structure

```
Flappy-bird-/
│
├── flappybird.py         → Main game script
├── background.png        → Background sprite
├── ground.png             → Ground sprite
├── pipe.png               → Pipe sprite
├── pipe_body.png          → Pipe body segment
├── pipe_end.png           → Pipe end cap
├── bird_wing_up.png       → Bird sprite (wing up)
├── bird_wing_down.png     → Bird sprite (wing down)
├── bird.gif               → Bird preview/demo
└── requirements.txt       → Python dependencies
```

## ⚙️ Setup

```bash
git clone https://github.com/shreyajainnx09/flappy-bird.git
cd flappy-bird

python3 -m venv .venv
source .venv/bin/activate      # on Windows: .venv\Scripts\activate

pip install -r requirements.txt
```

**`requirements.txt`**
```
pygame
```

## ▶️ Run

```bash
python3 flappybird.py
```

## 🧠 How It Works

- The bird falls continuously under a constant **sink speed** (gravity).
- Pressing the flap key/mouse button triggers a short **climb** phase, easing the bird upward over a brief duration before gravity takes back over.
- Pipe pairs spawn at a fixed interval and scroll left across the screen at a constant speed.
- Collision is checked with pixel-accurate masks between the bird sprite and the pipes/ground.
- Score increments each time the bird clears a pipe pair.

## 🌟 Ideas for Extending

- Add a difficulty ramp (pipes speed up / gaps shrink as score increases)
- Persist and display a local high score
- Add sound effects for flapping, scoring, and collisions
- Add a start screen and a proper game-over/restart screen
- Animate the bird's wing-flap based on velocity rather than a fixed timer

## 👩🏻‍💻 Author

**Shreya Jain**
BCA | Data Analytics | Python | SQL | Tableau
