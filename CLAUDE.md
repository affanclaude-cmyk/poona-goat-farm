# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-page marketing website for Poona Goat Farm — a premium goat farming business in Pune. Built as a standalone `index.html` file using Tailwind CSS (CDN) with Material Symbols icons and Google Fonts.

## Tech Stack

- **Tailwind CSS** via CDN (`https://cdn.tailwindcss.com?plugins=forms,container-queries`) with a custom config block in a `<script id="tailwind-config">` tag
- **Google Fonts**: Manrope (headings), Inter (body)
- **Material Symbols Outlined** icon font
- **No build step** — pure HTML, open directly in browser

## Key Architecture Notes

- The Tailwind config is inlined in a `<script id="tailwind-config">` tag in `<head>` — custom colors use hex values not mapped to standard Tailwind palette
- Custom CSS classes (`soft-lift`, `forest-shadow`, `signature-gradient`) are defined in a `<style>` block
- Images are either local (`images/hero.png`, `images/distance_view.png`) or external Google Photos URLs
- Phone number (`7722000786`) and WhatsApp links use `tel:+917722000786` and `https://wa.me/917722000786`
- Mobile-first: horizontal overflow issues are a recurring concern — `overflow-x: hidden` on `body` and `html`, `max-width: 100%` on images, and `overflow-hidden` on all major sections are the standard mitigations applied

## Commands

- **Open locally**: just open `index.html` in any browser
- **Mobile testing**: use Chrome DevTools device toolbar (F12 → Toggle device toolbar)
- No build, lint, or test commands — single HTML file project

## File Structure

```
index.html          — the complete website (HTML, CSS, JS config all in one file)
images/
  hero.png          — hero banner image
  distance_view.png — farm distance/lifestyle image
```
