# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static corporate landing page for Blackrock Group PTY LTD. The entire site is a single file: `index.html` with embedded CSS and JavaScript. No build pipeline, no frameworks.

## Commands

```bash
npm start       # Serves the site at http://localhost:3000 (runs: npx serve . -l 3000)
npm install     # Installs the `serve` dependency
```

No test suite exists.

## Architecture

All code lives in `index.html`:

- **CSS**: Uses CSS custom properties defined in `:root` for the full color palette (black/charcoal/stone/gold/cream). All responsive layout is handled with a single breakpoint at `max-width: 900px`.
- **HTML**: Five `<section>` elements — hero, services, about, contact, footer — each isolated and independently styled.
- **JavaScript**: One function, `handleSubmit()`, handles the contact form client-side (no backend — shows a success message and resets after 3 seconds).

## Deployment

Configured for nixpacks-compatible platforms (Railway, etc.) via `nixpacks.toml`. Build runs `npm install`, start runs `npm start`.
