---
title: "Flap"
description: "A Flappy-Bird-style arcade game built for this site — difficulty ramp, power-ups, a local leaderboard, and a parallax background, all in a single vanilla-JS canvas."
link: "https://ravenmoray.github.io/play/"
tags: ["game", "canvas", "javascript"]
date: 2026-08-23
---

A small arcade game built straight into this site's `/play` page — no game engine, just a `<canvas>` and vanilla JavaScript.

Features:
- Difficulty ramps up as your score climbs (faster scroll, tighter gaps), with a floor so it never becomes unfair.
- Power-ups: a shield that absorbs one hit, a slow-mo window, and a double-points window.
- A local top-5 leaderboard (saved in your browser) with classic arcade-style initials entry.
- A parallax background with three independently-scrolling layers, drawn entirely on the game's own canvas.
- Oscillating pipes mixed in with static ones as the difficulty increases.

Built collaboratively with Claude Code, including a full manual playtest pass to tune the numbers.
