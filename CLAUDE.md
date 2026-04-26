# CLAUDE.md

This file provides guidance to Claude Code when working with code in this repository.

## Who You're Working With

Rob is the owner/builder of this project. He's not a developer — always explain things in plain English. Use British spelling throughout (organise, colour, recognise). Warm, direct tone. No jargon, no filler, no preambles. Never delete, send, or publish anything without his explicit confirmation.

## Project History & Memory

Full project history and session notes are kept at:
`/Desktop/CLAUDE COWORK/Projects/Blackrock Group/memory.md`

Read this file at the start of every session to get up to speed. Update it at the end of the session with what was done and what's next.

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
