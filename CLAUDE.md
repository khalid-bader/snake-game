# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file snake game written in vanilla HTML/CSS/JavaScript. No build process, dependencies, or external frameworks.

## Opening the Game

Open `snake.html` directly in any web browser. No server required.

## Game Controls

- **Arrow keys or WASD** — move the snake
- **Space or Enter** — start game or restart after game over

## Code Structure

All logic is in `snake.html`:
- **Canvas drawing** — 500×500px grid (20×20 cells, 25px each)
- **Game loop** — `requestAnimationFrame` with timestamp-based timing
- **Snake mechanics** — array of {x, y} cells, head moves first, body follows
- **Collision detection** — walls and self-collision end game
- **Apple spawn** — random location, never on snake body

## Key Performance Notes

- Rendering uses `canvas` for speed (no DOM manipulation)
- Speed increases with score (60ms to 150ms per frame)
- Grid lines drawn for visual clarity, can be removed from `draw()` if needed
- No comments in code per requirements — logic is straightforward

## Customization

Easy adjustments at top of script:
- `CELL = 25` — cell size in pixels
- `COLS/ROWS = 20` — grid dimensions
- `BASE_SPEED = 150` — starting frame interval in ms
- Colors in `draw()` and CSS
