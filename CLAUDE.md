# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of educational mini games for kids, currently featuring a dot counting game. The project is built as static HTML/CSS/JavaScript files that run locally in a browser.

## How to Run

Since this is a static HTML project with no build system:

1. **Local Development**: Open `index.html` in a browser to access the game selection menu
2. **Individual Games**: Open specific game files like `counting.html` directly in a browser
3. **Local Server** (optional): Use any local server like `python -m http.server 8000` to serve files

## Project Structure

- `index.html` - Main entry point with game selection menu
- `counting.html` - Dot counting game implementation
- `docs/` - Documentation folder containing game specifications
- `README.md` - Basic project description

## Code Architecture

### Static HTML/CSS/JavaScript Architecture
- **No build system** - All code is vanilla HTML, CSS, and JavaScript
- **Self-contained games** - Each game is a complete HTML file with embedded CSS and JavaScript
- **No external dependencies** - Uses only browser APIs and vanilla JavaScript

### Game Structure Pattern
Each game follows this pattern:
- Complete HTML document with embedded styles and scripts
- Multiple view states (start screen, game screen, result screen)
- Game logic contained within `<script>` tags
- CSS for styling and animations embedded in `<style>` tags

### Dot Counting Game (`counting.html`)
- **Game Logic**: JavaScript functions for dot generation, positioning, and answer checking
- **UI States**: Start view, game view, timed mode, and result screens
- **Game Flow**: 
  - Generates 3-5 dot groups with 1-6 dots each
  - Provides 4 multiple choice options
  - Allows up to 3 retries on wrong answers
  - Includes both regular and timed modes
- **Styling**: CSS grid patterns for dot positioning (dice-like layouts)

## Development Guidelines

- Games are self-contained HTML files - no shared libraries or frameworks
- Use vanilla JavaScript - no external JavaScript libraries
- Embed CSS directly in HTML files using `<style>` tags
- Follow existing naming conventions for CSS classes and JavaScript functions
- Each game should include an exit button to return to the main menu (`index.html`)

## Testing

Manual testing only - open files in browser and test functionality. No automated test framework is configured.