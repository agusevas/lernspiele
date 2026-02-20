# Lernspiele

Educational games platform for kids (ages 6-10). German UI, English code/comments.

## Tech Stack

Vanilla HTML/CSS/JS. No build tools, no dependencies, no frameworks.

## How to Run

Open `index.html` in a browser. No build step needed.

## Project Structure

```
index.html              # Landing page (links to all games)
mathe-stars/index.html  # Math arithmetic game
wuerfelnetze/index.html # Cube net spatial reasoning game
wortreich/index.html    # German grammar game (cases & irregular verbs)
```

Each game is a **single self-contained HTML file** with inline CSS and JS. No shared code between games.

## Code Conventions

- **Single-file architecture**: All HTML, CSS, and JS in one file per game
- **JS namespaces**: Code organized as object literals — `Storage`, `Achievements`, `UI`, `GameEngine`, `App`
- **CSS**: kebab-case classes, CSS custom properties for theming (`--primary`, `--bg`, etc.)
- **JS**: camelCase variables/functions
- **German** user-facing text, **English** code identifiers and comments
- **SPA navigation**: Screen-based with `.hidden` class toggling (`display: none !important`)
- **Container**: `#app` with `max-width: 480px`, mobile-first design

## Game Screen Flow

Welcome → Home → Mode Select → Countdown → Game → Results

Additional screens: Stats, Achievements, Settings

## Data Persistence

- localStorage with JSON serialization
- Single key per game (`mathStars`, `wuerfelnetze`, `wortreich`)
- `Storage` object handles load/save/reset
- Auto-save on state changes

## Styling Patterns

- CSS variables for per-game theming
- Google Fonts on landing page (Fredoka, Nunito); system fonts in games
- Mobile-first, 480px max-width container
- Transitions/animations for screen changes and feedback
