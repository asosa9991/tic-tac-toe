# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a modern, single-file Tic Tac Toe web application. It features responsive design, win-state animations, and session-based score tracking.

## Development Commands
As a single-file static web application, there is no build or compilation step.

- **Run/View:** Open `tic-tac-toe.html` in any modern web browser.
- **Lint/Format:** No automated tools configured. Follow existing indentation (4 spaces) and naming conventions.
- **Git Workflow:** Commit changes regularly with clean, descriptive commit messages. Push to GitHub (`origin main`) frequently to ensure state is never lost.

## Architecture
The application follows a monolithic structure within a single HTML file:

- **UI/Styles:** Embedded `<style>` block using CSS Grid for the game board and Flexbox for layout. Responsive design via media queries.
- **DOM Structure:** Simple container-based layout with a `#board` div for the grid and `#status` for game state messaging.
- **State Management:**
  - `gameBoard`: 1D array of 9 strings representing the 3x3 grid.
  - `currentPlayer`: Tracks 'X' or 'O'.
  - `gameActive`: Boolean flag to control gameplay flow.
  - `scores`: Object tracking session wins.
- **Logic Flow:**
  - `createBoard()`: Initializes/resets the DOM elements for the board.
  - `handleCellClick()`: Primary event handler for player moves; triggers win/draw checks.
  - `checkWin()` / `checkDraw()`: Logic for determining game termination.
