# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static landing page for a premium apartment rental at **Torres del Poeta**, La Paz, Bolivia. Deployed on Vercel as a static site (no build step, no bundler, no package.json).

## Development

- **No build system** — open `index.html` directly in a browser or use any local server (e.g., `npx serve .`, `python -m http.server`)
- **Deploy:** `vercel` CLI from the project root, or push to GitHub for automatic Vercel deployments
- **No tests or linting** configured

## Architecture

The entire site lives in a single `index.html` (~1950 lines) structured as:

1. **`<head>`** — SEO meta/Open Graph, Schema.org structured data, TailwindCSS via CDN (`cdn.tailwindcss.com?plugins=forms,typography`), Google Fonts (Playfair Display + Inter), Material Symbols Outlined, inline Tailwind config, and all custom CSS (`<style>` block)
2. **`<body>`** — Semantic HTML sections: Header (fixed, glassmorphism), Hero Carousel, Stats, Gallery, Building Amenities, Pricing, Trust Badges, Footer, Sticky CTA bar, Lightbox modal
3. **`<script>` blocks** (4 total, inline at bottom):
   - **i18n system** — `translations` object with keys for ES/EN/FR/PT; uses `data-i18n` attributes on elements; persists language choice in `localStorage`
   - **Carousel** — object-literal pattern controlling 8 slides with opacity transitions, autoplay (15s), dots, touch/swipe support
   - **Lightbox** — collects gallery images, full-screen overlay with keyboard navigation (Escape/Arrow keys)
   - **Scroll Reveal + Sticky CTA** — IntersectionObserver adds `.visible` to `.reveal` sections; mobile sticky bar appears after scrolling past hero

## Key Conventions

- **Tailwind config** is inline in a `<script>` tag — custom colors: `primary` (#C5A059 gold), `primary-dark`, `navy-900/800/700`; custom fonts: `font-display` (Playfair Display), `font-sans` (Inter)
- **i18n:** all translatable text uses `data-i18n="keyName"` attributes. Add new strings to the `translations` object for all 4 languages (es, en, fr, pt)
- **Images:** local files in `images/hd/` and `images/hd/hd2_amoblado/`. Hero carousel uses 8 images with lazy loading (except first). Gallery images are clickable (lightbox)
- **WhatsApp CTA:** links use `wa.me/59172004767` — the real contact number
- **CSS animations:** custom keyframes for pulse, shimmer, urgency badge, price glow, fade-in-up, and scroll reveal — all defined in the `<style>` block
- **Mobile-first:** sticky CTA bar hidden on `md:` breakpoint; responsive layout via Tailwind utilities

## Source Variants

`src/stitch_premium_apartment_listing_v1/` contains 10 original design variants (code.html + screen.png) used as reference during development. These are not served in production.
