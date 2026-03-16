---
phase: quick
plan: 260315-vi1
subsystem: bracket-picker
tags: [march-madness, toddler-app, single-file, offline, ipad]
dependency_graph:
  requires: []
  provides: [bracket-picker-app]
  affects: []
tech_stack:
  added: [vanilla-html, vanilla-css, vanilla-js]
  patterns: [single-file-app, css-animations, state-machine]
key_files:
  created:
    - /Users/tzulueta/app/index.html
  modified: []
decisions:
  - Randomized left/right team placement to prevent bias in toddler picks
  - Used CSS dot/confetti animations instead of emoji celebrations for clean UI
  - Single emoji per team as mascot identifier, no emoji clutter
  - Equal-weight color pairs (no red=bad/green=good bias)
  - Seed numbers shown small and low-opacity to avoid implying team quality
metrics:
  duration: 173s
  completed: 2026-03-15
---

# Quick Task 260315-vi1: March Madness Mascot Bracket Picker Summary

Single-file bracket picker (877 lines) for toddler iPad use with randomized team placement, CSS confetti animations, and printable bracket output.

## What Was Built

A complete March Madness 2026 bracket picker in a single `index.html` file, optimized for a 2-year-old on iPad. The app presents two large, equally-weighted mascot cards per matchup. The toddler taps to pick winners through all 6 rounds (64 games total), then a printable bracket is generated.

### Key Features
- 68 teams across 4 regions (East, West, South, Midwest) with correct seeding
- Randomized left/right card placement per matchup (no positional bias)
- Equal visual weight: same card size, same brightness, distinct but balanced color pairs
- One emoji per team as a simple mascot identifier (clean, not cluttered)
- CSS-only confetti particles on each pick (no emoji celebration screens)
- CSS dot animations for round transitions (no party emoji)
- Champion screen with pulsing animation and gradient text (CSS, not emoji)
- Full 6-round progression: Round of 64 through Championship (32+16+8+4+2+1 = 63 games)
- Printable bracket view with landscape @media print styles
- Zero external dependencies, fully offline
- Touch-optimized: no scroll, no zoom, large tap targets, overscroll prevention

## Task Completion

| Task | Name | Status | Commit | Files |
|------|------|--------|--------|-------|
| 1 | Build complete bracket picker app | Complete | b3f3702 | index.html |
| 2 | Human verification checkpoint | Awaiting | - | - |

## Deviations from Plan

### User Feedback Incorporated (Overrides Plan)

**1. No emoji overload** - Plan called for emoji party celebration screens. Replaced with CSS dot animations and color-based confetti.

**2. Unbiased presentation** - Plan showed teams in fixed seed order. Added Math.random() side-swapping so team placement is randomized per matchup. Both cards have identical sizing and balanced color pairs.

**3. Clean UI** - Seed numbers rendered small with 50% opacity. No color coding that implies team quality. One emoji per card as identifier only.

## Verification Results

- File exists: PASS (877 lines)
- All 4 region teams present: PASS
- All 6 round names: PASS
- Print media query: PASS
- Viewport meta: PASS
- Confetti animation code: PASS
- No external URLs: PASS (zero http/https references)
## Self-Check: PASSED
