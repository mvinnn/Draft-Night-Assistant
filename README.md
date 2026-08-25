# Draft-Night-Assistant

A live companion for the Bozo Club fantasy draft on Sleeper. Syncs to the
real draft room and tells you who to pick — it never submits a pick for
you, that always happens in Sleeper itself.

**Live:** https://mvinnn.github.io/Draft-Night-Assistant/

## Using it

Open the link above and paste your Sleeper draft URL into "Sleeper live
sync" (either format works, e.g. `sleeper.com/draft/nfl/<id>` or
`sleeper.com/beta/draft/nfl/<id>`).

To send someone a link that configures itself automatically, add their
draft and Sleeper username as URL params:

```
https://mvinnn.github.io/Draft-Night-Assistant/?draft=<draft_id>&user=<sleeper_username>
```

That auto-connects to the draft and figures out their pick slot on its
own — no setup needed on their end.

By default the app shows one plain-language card: who to pick and why.
Tap "Show details" for the full board, tiers, alerts, and roster plan.

## Notes

- No backend — talks to Sleeper's public API directly from the browser.
- Rankings, tiers, and target/avoid calls are from Joel Smyth's 2026 PPR
  Draft Guide, embedded in `index.html`.
- Sleeper's public API is CDN-cached (~30s), so live sync can lag a bit
  behind the actual draft room — use "Refresh now" or manual entry right
  before your pick if it matters.
