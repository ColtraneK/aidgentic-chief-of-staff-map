---
name: wrap-up
description: Close a working session — log what happened, and write anything durable that was learned back into Business Context.md so the system is smarter next time rather than just longer. Trigger when the user says "wrap up", "done for the day", "that's it for today", "end of day", "log this", "we're finished", "goodnight", or otherwise signals they're closing out. Only fires when a Chief of Staff workspace exists — an attached Project or selected folder containing CLAUDE.md or Business Context.md; if another installed plugin also claims these phrases, that workspace is the tiebreaker. If a session is clearly ending without them saying so, offer it once.
---

# Wrap Up

Two jobs, and the second one is the one that matters.

**The log** records what happened. **The write-back** takes what was learned about the business and puts it where every future session will read it. A system that only logs gets longer. A system that writes back gets smarter.

Read `${CLAUDE_PLUGIN_ROOT}/reference/voice-and-ground-rules.md` first.

---

## Step 1 — The log

Review the session and pull out what a colleague taking the next shift would need. Save to `03 Session Notes/[YYYY-MM-DD].md`:

```markdown
---
date: YYYY-MM-DD
---

# Session — [Weekday, Month DD]

## What we did
- [3–6 tight bullets]

## Decisions made
- [the decision — and what it rules out]

## Still open
- [what's mid-flight, and what it's waiting on]

## Pick up here
[1–2 sentences]
```

Skip **Decisions made** or **Still open** entirely if there's nothing real in them. Don't invent open items to fill a heading.

**A second wrap-up on the same day adds to that day's file**, under its own `# Session` heading below the first. Never overwrite it: the morning's session is in there.

---

## Step 2 — The write-back

This is the part that compounds. Go back through the session and pull out anything true about the **business** rather than about the session, then write it into `Business Context.md`:

| What came up | Where it goes |
|---|---|
| A new client, funder, partner or counterparty | **People** → Active (or **Who Matters**, if the deep read hasn't run yet) |
| A date that can't move | **Fixed Points** |
| A correction — "no, that's not how we do it" | **Corrections** |
| A word they used that you'd been getting wrong | **Vocabulary** |
| A change in how money flows | **What Money Looks Like** |
| A system you can't see into | **Blind Spots** |
| A standing meeting or rhythm | **Rhythm** |
| A job they taught you this session | the Playbooks table in `CLAUDE.md` |
| A suggestion you made under ground rule 10, and what they said | **Already Suggested** |
| A reaction to a primer — "more of that", "not interested in X", "cover Y next" | `Learning Log.md` → **What they've said** |

**Corrections are the highest-value entries in the file.** Every time they tell you something is wrong, that's a permanent upgrade — as long as it gets written down. Date each one and record what was assumed alongside what's actually true.

Add, never rewrite. If something is superseded, move the old version to **Corrections** with the date rather than deleting it.

Then say in one line what you saved. They should be able to see the system got smarter without opening the file.

---

## Step 3 — Flag the drift

Only reported when they fire, and only the ones wrap-up owns under ground rule 11. Circling belongs to the Sunday review and a missed primer to the next brief, so neither is repeated here. The offers below are one chance each: check **Already Suggested** first, and record what you said and what they answered.

**Stale picture.** If `Standing Map.md` — the dashboard's saved state — is more than 8 days old, the interesting fact is usually that Sunday's review didn't run, not that the map is old. **Check before you say it:** look at what's scheduled. If the Sunday task is missing, it was part of setup, so offering to put it back is a repair rather than a new suggestion: *"Your map is eleven days old because the Sunday review isn't on your schedule any more. Want it back, same time?"* A yes recreates it per `scheduled-runs.md`. If it's there, say it didn't produce a map and that the next brief will show whether it recovers. Don't rebuild it now; they're leaving. If they decline putting it back, record that and don't raise the stale map again.

**Old working file.** If `CLAUDE.md` carries a template stamp older than **v2.0**, offer the update once, in one clause — *"your working file is from an older version; say the word and I'll bring it current, keeping everything you've added."* Record the answer, so it's never offered again after a no.

**A context file that's outgrown itself.** The People tiers keep themselves tidy, so this only fires when something else has bloated — a year of individual Corrections, or session detail recorded in the wrong file. One clause, once ever, and only when it's true. See *Keeping the file worth reading* in the **business-context** skill.

**Standing work that isn't moving.** If a standing task has run five or more times with nothing changing, and the Sunday review hasn't already offered it, name it once and offer to retire it, per the **standing-work** skill. One line, no pitch.

---

## Step 4 — Record what you suggested

If you made a suggestion this session under ground rule 10, write it into `Business Context.md` under **Already Suggested**, with the date and what they said:

```markdown
## Already Suggested
- [YYYY-MM-DD] Connecting their books — [declined / said later / done]
```

This is what stops the same observation coming back next week. Ground rule 10 gives connectors and skills one chance each; this file is the only thing that remembers it was used. Record a declined **proposal** here too, under rule 10 — an offer they turned down shouldn't come back next Tuesday.

**Don't make a new suggestion here.** They're leaving. If something's worth saying, it was worth saying while they were still working.

---

## Step 5 — Catch the dates before they leave

**The one exception to the rule above**, and it's narrow: if a **date** was committed to during this session — they said they'd have something to someone by a day, agreed to a deadline, or mentioned a date in passing — offer the reminder now, in one line.

This isn't a new suggestion. It's closing the loop on something that happened while they were here, and the alternative is that the commitment goes into a session note nobody reads until it's late.

> "You told Priya the scope by the 14th. Want a nudge on the 12th?"

Rules: **one**, the most consequential if there were several. Declinable in a word. Skip it entirely if `Standing Work.md` already has a reminder covering that date. And if they say yes, create it per the **standing-work** skill — it doesn't cost a standing slot, so don't mention the cap.

---

## Close

Two lines maximum. Where the log went, what you saved into context, and the one place to pick up. They're done for the day — respect that.

Never end with encouragement.
