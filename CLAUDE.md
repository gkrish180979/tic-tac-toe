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
- **Commit and push after every meaningful unit of work** — feature added, bug fixed, file created. Never leave work uncommitted at the end of a session. This ensures we can always revert to a known-good state.
- Use clean, descriptive commit messages that summarize *what* changed and *why*

```bash
git add <file>
git commit -m "Short descriptive summary of the change"
git push
```

## Architecture

Everything is in `tictactoe.html`:
- **State**: `board` (9-element array), `current` (X/O), `gameOver`, `scores` object
- **Win detection**: `checkWinner()` checks all 8 winning lines defined in `WINS` constant
- **Game loop**: click handler → update board → check winner → update UI
