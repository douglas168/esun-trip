# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-page static site comparing 玉山主峰 (Jade Mountain) guided tour operators for a friend group trip in 2026. Published via GitHub Pages.

- Live URL: https://douglas168.github.io/esun-trip/
- GitHub repo: https://github.com/douglas168/esun-trip

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main comparison page (all CSS and JS inline) |
| `line-message.md` | LINE group messages — welcome + date availability poll |
| `dates-submitted.md` | Submitted date availability responses from group members |
| `tour-operators.md` | Tour operator research data |
| `list-dk.md` | DK's personal registration info |
| `list-stanley.md` | Stanley's LINE chat log / group messages |
| `registration.csv` | Consolidated participant registration data |
| `user-input.md` | Source URLs — **untracked, do not commit** |

## Deployment

Push to `main` → GitHub Pages auto-deploys. No build step.

```sh
git push origin main
```

## Architecture

`index.html` is self-contained: inline `<style>`, inline `<script>`, no external dependencies except Google Fonts (if any). CSS custom properties are defined in `:root` for color theming:

- `--taichung` (blue): 台中高鐵 departure
- `--chiayi` (green): 嘉義出發
- `--both` (purple): either departure point
- `.hl-kaohsiung` (orange-red): 高雄高鐵 departure

The quick-compare table columns (in order): 業者 · 行程天數 · 費用 · 集合地點/時間 · 行程概要 · 餐食 · 成團人數 · 評價&口碑.

## Context

See `HANDOFF.md` for session history and pending decisions (LINE message opening line, permit booking).
