# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-file web game project. All code lives in `tictactoe.html` — HTML, CSS, and JavaScript are all inline in one file. No build system, no dependencies, no package manager.

## Running the Project

Open `tictactoe.html` directly in a browser:
```bash
open tictactoe.html
```

## Git & GitHub Workflow

- `~/bin/gh` is the GitHub CLI (installed locally, not system-wide)
- Remote: https://github.com/gkrish180979/tic-tac-toe
- After every change: commit with a descriptive message and push to `main`

```bash
git add <file>
git commit -m "Description of change"
git push
```

## Architecture

Everything is in `tictactoe.html`:
- **State**: `board` (9-element array), `current` (X/O), `gameOver`, `scores` object
- **Win detection**: `checkWinner()` checks all 8 winning lines defined in `WINS` constant
- **Game loop**: click handler → update board → check winner → update UI
