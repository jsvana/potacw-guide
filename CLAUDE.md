# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-page static HTML site — a field manual for operating CW (Morse code) in the Parks on the Air program. Hosted at `potacw.guide` via GitHub Pages.

## Architecture

The entire site is one file: `index.html`. All CSS is inlined in a `<style>` block. No build step, no JavaScript, no framework. Just open the file in a browser.

## Design System

The site uses a typographic "field manual" aesthetic with CSS custom properties:

- **Fonts**: Fraunces (headings), Source Serif 4 (body), Archivo (labels/uppercase), JetBrains Mono (code/CW text) — loaded from Google Fonts
- **Palette**: `--paper` (warm cream), `--ink` (dark green-black), `--moss` (green accents), `--tan-deep` (brown accents), `--brick` (red highlights for CW prosigns)
- **Components**: `.plate` (masthead), `.chapter` (section headers with roman numerals), `.card` (role descriptions), `.qso` (exchange transcript), `.aside` (margin notes), `.freqs` (frequency table), `.steps` (numbered procedure list), `.logbook` (sample log), `.colophon` (footer attribution)

## Conventions

- CW (Morse) text uses the `.cw` class with `--mn` (monospace) font
- Highlighted CW elements use `.hl` (brick color)
- Section numbers are roman numerals in `.chapter .num`
- All content is static — no dynamic rendering
