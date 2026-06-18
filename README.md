# Wordle Group Tracker

A lightweight single-file web app for tracking Wordle scores with your Discord friend group.

## Features

- **Leaderboard** — Valorant-style table with sortable columns, player color accents, and smooth shuffle animations when resorting
- **Board** — detailed player cards with guess distribution charts, weighted averages, and stat breakdowns
- **History** — full game log with calendar heatmap, filterable by player and month, inline score editing
- **Log Results** — paste your Discord Wordle activity message directly and it auto-parses scores and dates
- **Players** — manage your roster; upload profile photos per player (stored as base64 in your data file)

## How It Works

Paste the Discord activity message (e.g. `4/6: @player1 X/6: @player2`) into the Log tab and hit Preview → Confirm. Scores are parsed automatically and saved locally.

### Scoring

Weighted average penalizes both failed (`X/6`) and missed days equally at a weight of 7, so consistent participation is rewarded alongside raw solving ability.

## Data Storage

- **Local** — data saves to `localStorage` by default. Use the "Link a file" option (Chrome/Edge) to auto-save to a `.json` file on disk.
- **Deploy** — export `data.json` from the Log tab and commit it alongside `index.html` to your repo. The live site loads it in read-only view mode automatically.

## Live Site

Deployed via Vercel at: https://discord-wordle-with-friends.vercel.app

## Stack

Vanilla HTML/CSS/JS — no build step, no dependencies, single file.
