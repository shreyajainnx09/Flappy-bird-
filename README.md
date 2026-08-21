# Flappy Bird 🐦

A Python clone of the classic *Flappy Bird* game, built with [Pygame](https://www.pygame.org/). Flap the bird through a stream of pipes without hitting them or the ground — the longer you survive, the higher your score.

## Gameplay

- The bird continuously sinks toward the ground under gravity.
- Click the mouse, or press **Up Arrow**, **Enter**, or **Spacebar**, to make the bird climb.
- Pipes scroll in from the right at a steady pace, spawning at a fixed interval, with a randomized gap.
- Score increases by 1 each time the bird passes a pipe.
- The game ends if the bird hits a pipe, the ground, or the top of the screen.

## Controls

| Action | Key |
|---|---|
| Flap / climb | `Space`, `Enter`, `Up Arrow`, or mouse click |
| Pause / resume | `P` or `Pause` |
| Quit | `Esc` or close the window |

## Requirements

- Python 3
- [Pygame](https://www.pygame.org/)

Install Pygame with:

```bash
pip install pygame
```

## Running the game

```bash
python flappybird.py
```

## Project structure

```
Flappy-bird-/
├── flappybird.py       # Main game script (Bird, PipePair classes, game loop)
├── background.png      # Background image
├── ground.png           # Ground image
├── bird.gif             # Bird animation preview
├── bird_wing_up.png     # Bird sprite (wing up)
├── bird_wing_down.png   # Bird sprite (wing down)
├── pipe.png              # Pipe sprite
├── pipe_body.png         # Pipe body segment
└── pipe_end.png           # Pipe end cap
```

> **Note:** `flappybird.py` loads images from an `images/` subfolder by default. If you keep the image files in the project root, either move them into an `images/` folder or update the paths in the `load_images()` function accordingly.

## How it works

- **`Bird`** — a `pygame.sprite.Sprite` that tracks its vertical position, animates between two wing frames, and uses a cosine-eased climb when flapping, otherwise sinking at a constant speed.
- **`PipePair`** — generates a top and bottom pipe with a randomized gap large enough for the bird to pass through, and scrolls leftward each frame.
- **`main()`** — runs the game loop: spawns pipes at a fixed interval, handles input, checks collisions (via pixel-perfect mask collision), draws each frame, and tracks/display the score.

## License

No license specified. Add one if you plan to share or accept contributions.
