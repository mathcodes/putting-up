# Putting Up

A live, phone-friendly tool for APA team captains to put up players under the **23 rule** — each team's 5 players' skill levels can't total more than 23.

[LIVE](https://mathcodes.github.io/putting-up/)

## Layout
The page has two independent copies of the tool, each with its own rosters, lineup and saved data:
- **8-Ball** on top (SL 2–7)
- **9-Ball** below (SL 1–9)

Each section has a ball banner, its own **📋 Paste matchup** button, and instructions for copying the matchup from league.poolplayers.com. If you paste a 9-ball matchup into the 8-ball section (or the other way round), it warns you and offers to load it into the right section.

A **🔗 Links** section at the bottom collects league bylaws, APA/BCA rules, instruction (Dr. Dave) and community resources.

## What it does
- Two team rosters (name + skill level), up to 8 players each.
- 5 match slots (configurable); tap a player to put them up in the highlighted slot.
- Running total vs. the cap for each team, room left, slots left, and **max SL allowed next**.
- Players already played that night are greyed out and removed from the pool.
- Players who **can't** play are redded out: a player is ineligible if their SL plus the cheapest possible fill for the remaining slots would push the team over the cap (so it warns you *before* you paint yourself into a corner).
- "Not here" toggle (💤) for absent players; forfeit warning if you run short.
- Alternating "who puts up first" indicator per match (⇄ to swap).
- Cap is editable per section.
- "New night" clears matches but keeps rosters. Everything saves in the browser (localStorage).

## Paste a matchup
Tap **📋 Paste matchup**, then paste the matchup page from poolplayers.com (from the date down through the last away player). It picks up:
- Home and away team names, team numbers (e.g. #93704) and division team numbers (04)
- Every player's name, member #, skill level, and season stats (W/P, win %, PPM, PA)
- Match date, time, venue, div reps, scored/scoresheet status
- Format (9-ball vs 8-ball), detected from skill levels and PPM

You get a preview before it loads. A single team's roster table also works; you choose Home or Away.

## Run
No build step — it's a single static file.

```bash
open index.html          # or: npx serve .
```

Live on GitHub Pages: **https://mathcodes.github.io/putting-up/**

Every push to `main` redeploys automatically via `.github/workflows/pages.yml`. If the first run fails at *configure-pages*, go to **Settings → Pages → Build and deployment → Source: GitHub Actions**, then re-run the workflow.
