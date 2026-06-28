---
description: Log a durable decision (D-NNN) to the decision log, or review decisions due for re-confirmation
---

Maintain `brain/decisions/decision-log.md` — the append-only record of decisions that
shape work (methodology, scope, stakeholder, commercial, ways-of-working). Read that
file's header for the conventions before writing. Handle directly (no sub-agent).

## Mode A — log a decision (default, when given a decision)
1. Read `brain/decisions/decision-log.md` to find the highest `D-NNN`; the new entry is
   the next number, today's date, inserted at the **top** of the log.
2. Fill every field of the entry shape. Infer what you can from the brain; **ask {{OWNER}}
   only for what you genuinely can't infer** — usually just the **`Review by`** date
   (propose one: ~90 days for methodology/scope, sooner for stakeholder calls, `—` for
   durable structural choices) and the owning **project**.
3. **Cross-post** so the decision is findable from where he'll look:
   - Append a matching dated line to the project's `## Decisions & assumptions`
     (and, if it changes a load-bearing number, the project's **Current truth** block).
   - Add a one-liner to today's `brain/daily/` log.
4. If this decision **reverses or revises** an earlier one, flip that entry's `Status`
   to `Superseded by D-NNN` (the only edit allowed on a past entry) and say which.
5. Confirm in 1-2 lines: the `D-NNN`, the review date, and where it was cross-posted.

## Mode B — review (`/decision-log review`)
Apply the **anti-anchor rule**: don't trust the snapshot, re-derive status.
1. List **Active** entries whose `Review by` is past or within 14 days, plus any that
   look stale against the latest daily logs / project state.
2. For each, give a one-line "still true? / looks superseded by X / re-confirm" call.
3. Offer to update statuses or log superseding decisions. Don't edit without his go.

## Mode C — show (`/decision-log` with no args)
Print the most recent ~5 Active entries, newest first. Tight, scannable.

Decision to log / command: $ARGUMENTS
