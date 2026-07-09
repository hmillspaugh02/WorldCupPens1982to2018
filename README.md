# World Cup Penalty Shootouts

## What this is

I took every penalty from World Cup shootout history (305 shots, minus a few with missing data) and looked at where people actually shoot, whether they scored, and — the real question — whether any of it holds up statistically once you account for how small some of these samples are.

## The finding that matters

Shot zone doesn't really matter. Which way the keeper dives, by itself, doesn't matter either. What matters is whether the keeper guesses the **same side** as the shot: conversion drops from ~83% to ~54% when they guess right. That result is backed by 279 shots and a p-value around 0.0000005 — it's real.

Everything else in here — "best zone," lefty vs. righty splits — looks interesting in a bar chart but falls apart under a basic significance test (p-values of 0.4-0.75), usually because some of those cells only have 2-5 shots in them. I called that out explicitly rather than letting a flashy chart imply more than the data supports.

## What's in this repo

- `WorldCupShootouts.csv` — the raw shot-by-shot data
- `WCPenalties_Analysis.ipynb` — the whole analysis: goal-diagram heatmaps for shot placement, keeper dive vs. zone, foot splits, then Wilson confidence intervals and chi-square tests on all of it

Open the notebook to see the actual goal diagrams — reading a 3x3 grid of numbers is nowhere near as clear as seeing it drawn as a real goal with posts and a net.
