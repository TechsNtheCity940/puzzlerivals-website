# Puzzle Rivals Website

Public website and published Unity WebGL player for [puzzlerivals.com](https://puzzlerivals.com).

## Structure

- `index.html` and `style.css`: public landing page
- `game/`: production Unity WebGL build, deployed from the private source repository
- `CNAME`: GitHub Pages custom domain

## Deployment

The private repository `TechsNtheCity940/Puzzle_rivalS` contains the Unity project and production build at `Build/PuzzleRivals-WebGL`. Its GitHub Actions workflow publishes that directory into this repository's `game/` directory.

GitHub Pages must be enabled for this repository and configured to publish the `main` branch from the repository root.

The WebGL client is static content. Online matchmaking, player accounts, persistence, and authoritative multiplayer services require a separately hosted backend.
