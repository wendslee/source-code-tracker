# Source Code Daily Tracker

The canonical source for the Source Code Daily Tracker used by The Re-Awakening Portal.

## Project structure

- `public/index.html` contains the complete static application.
- `wrangler.jsonc` configures the existing Cloudflare Worker, `recode-tracker`, to serve the `public` directory.
- `sourcecodetracker.zip` is the original manual-upload archive retained temporarily for migration verification.

## Cloudflare deployment

This repository is prepared for Cloudflare Workers Builds:

- Build command: leave blank
- Deploy command: `npx wrangler deploy`
- Root directory: repository root

The app stores member entries in the member's browser using `localStorage` under the key `recode_v1`. A deployment replaces the application files but does not intentionally clear that browser data.
