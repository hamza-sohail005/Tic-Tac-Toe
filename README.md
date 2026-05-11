# Tic Tac Toe

A classic Tic Tac Toe game built with React 19 and Vite, featuring a glassmorphism UI, animated winner highlighting, and full move history with time travel.

**Live Demo:** [https://whimsical-marshmallow-24ea61.netlify.app/](https://whimsical-marshmallow-24ea61.netlify.app/)

## Features

- **Two-player gameplay** — Players alternate between X and O
- **Winner detection** — Automatically detects all 8 winning lines and announces the winner
- **Winning square highlight** — The three winning squares pulse with a glowing animation
- **Move history** — Every move is recorded in a sidebar list
- **Time travel** — Click any move in the history to jump back to that game state
- **Animated title** — Gradient color-shift animation on the game title
- **Glassmorphism design** — Frosted glass card on a deep navy gradient background
- **Hover & click animations** — Squares lift on hover and press on click

## Tech Stack

| Tool | Version |
|------|---------|
| React | 19 |
| Vite | 8 |
| JavaScript (JSX) | ES Modules |

## Project Structure

```
src/
├── App.jsx        # All game components (Square, Board, Game) and logic
├── index.css      # Global styles, animations, glassmorphism layout
├── App.css        # (reserved)
└── main.jsx       # React entry point
```

### Component Overview

- **`Square`** — A single cell button; receives its value, click handler, and a flag to apply the winner glow style
- **`Board`** — Renders the 3×3 grid, handles click logic, and derives the current status message
- **`Game`** — Root component; owns the move history state, drives time travel, and renders the move list sidebar
- **`calculateWinner`** — Pure helper that checks all 8 winning lines and returns the winner and winning indices

## Getting Started

**Prerequisites:** Node.js 18+

```bash
# Install dependencies
npm install

# Start the dev server
npm run dev

# Build for production
npm run build

# Preview the production build
npm run preview
```

The dev server runs at `http://localhost:5173` by default.

## How to Play

1. Player **X** always goes first
2. Click any empty square to place your mark
3. The first player to get three in a row (horizontally, vertically, or diagonally) wins
4. The winning squares will glow and pulse to highlight the result
5. Use the **Move History** panel on the right to jump back to any earlier state in the game
