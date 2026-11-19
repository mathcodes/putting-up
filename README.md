# Putting Up

A live, phone-friendly tool for APA team captains to put up players under the **23 rule** — each team's 5 players' skill levels can't total more than 23.

## What it does
- Two team rosters (name + skill level), up to 8 players each.
- 5 match slots (configurable); tap a player to put them up in the highlighted slot.
- Running total vs. the cap for each team, room left, slots left, and **max SL allowed next**.
- Players already played that night are greyed out and removed from the pool.
- Players who **can't** play are redded out: a player is ineligible if their SL plus the cheapest possible fill for the remaining slots would push the team over the cap (so it warns you *before* you paint yourself into a corner).
- "Not here" toggle (💤) for absent players; forfeit warning if you run short.
- Alternating "who puts up first" indicator per match (⇄ to swap).
- 9-Ball (SL 1–9) or 8-Ball (SL 2–7); cap is editable.
- "New night" clears matches but keeps rosters. Everything saves in the browser (localStorage).

## Run
No build step — it's a single static file.

```bash
open index.html          # or: npx serve .
```

Deploy anywhere static (Vercel: `vercel --prod` from this folder).
