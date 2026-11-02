# Puzzle Rivals Website

Public website and published Unity WebGL player for [puzzlerivals.com](https://puzzlerivals.com).

## Structure

- `index.html` and `style.css`: public landing page
- `CNAME`: GitHub Pages custom domain
- `game/`: production Unity WebGL build published by this repository's GitHub Pages workflow

## Deployment

The Unity source project lives in `TechsNtheCity940/Puzzle_rivalS`. A verified WebGL build is staged into this repository's `game/` directory, then a push to `main` triggers `.github/workflows/pages.yml` to publish the site through GitHub Pages.

The page keeps a browser-side gzip decoder for the compressed Unity data and WASM files because GitHub Pages does not provide configurable `Content-Encoding` response headers. The workflow validates gzip integrity and rejects the retired Tesana matchmaking endpoint before deployment.

Ranked four-player matches currently use local AI bot opponents by default. Live online matchmaking is a later phase and is not represented as available until a real online service is implemented.
