# Be My Valentine - Replit Agent Guide

## Overview

This is a simple, single-page Valentine's Day themed web application. It displays an animated, romantic "Be My Valentine?" page with sparkle effects, gradient backgrounds, and decorative typography. The app consists of a static HTML page served via a minimal Express.js server.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend
- **Single HTML file (`index.html`)**: Contains all markup, CSS styles, and presumably JavaScript (the file appears truncated but likely includes interactive elements like Yes/No buttons and animations).
- **Styling approach**: All CSS is embedded inline within `<style>` tags in the HTML file — no separate CSS files or build tools.
- **Fonts**: Uses Google Fonts (Dancing Script for headings, Quicksand for body text) loaded via `@import`.
- **Animations**: CSS keyframe animations for sparkle/twinkle effects and pulsing text. The design is heavily visual with gradients, text shadows, and decorative elements.

### Backend
- **Express.js (`server.js`)**: A minimal Node.js server that serves the static `index.html` file on the root route (`/`).
- **Port**: Runs on port 5000, bound to `0.0.0.0`.
- **No API routes**: The server only serves the single HTML file — there's no backend logic, database, or API endpoints.
- **No static file middleware**: Currently only serves `index.html` via `res.sendFile()`. If additional static assets (images, JS files, CSS files) are added, `express.static` middleware would need to be configured.

### Design Decisions
- **Why Express over just static files?**: Using Express allows easy expansion later (adding API routes, form handling, etc.) while keeping the setup simple.
- **Why inline styles instead of separate CSS?**: Keeps the project as simple as possible — everything in one file. For a small novelty page, this is fine. If the project grows, styles should be extracted.
- **No build tools**: No bundler, no TypeScript, no framework — just vanilla HTML/CSS/JS served by Node. This keeps things lightweight and easy to modify.

### Running the App
- **Dev command**: `npm run dev` (runs `node server.js`)
- The app will be available on port 5000.

## External Dependencies

### NPM Packages
- **express (^4.22.1)**: Web server framework for Node.js, used to serve the HTML page.

### External Services
- **Google Fonts CDN**: Dancing Script and Quicksand fonts are loaded from `fonts.googleapis.com` at runtime. Requires internet access for fonts to display correctly.

### Database
- None. This is a purely static/frontend application with no data persistence.