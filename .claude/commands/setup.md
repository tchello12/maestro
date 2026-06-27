---
description: First-run onboarding — welcomes the user, lists the brain files to fill, lets them pick where to start, then walks template-by-template filling every field (resumable, with a progress log)
---

You are running the **guided first-time setup**. Goal: take a brand-new user from a fresh
template to a live, *fully-populated* system — in a logical, friendly flow they control.

## STEP 1 — Welcome & explain (before ANY questions)
Open with a short, warm welcome (2–4 sentences, no questions yet). Explain plainly:
- What Maestro is, in one line (a chief-of-staff that remembers your context across days).
- **What setup actually is:** "We'll fill in a handful of Markdown files that are Maestro's
  memory — who you are, how you work, your cases, your goals. The more complete these are,
  the better Maestro works for you. It takes ~10 min and you can stop and resume anytime."
- Reassure: I'll ask in batches, give examples, and you can say "skip" on anything.

## STEP 2 — Show the files + suggested order, then ASK where to start (selectable)
Read `brain/setup-progress.md` (create it from the template if missing) and show the list
of files to fill **with their current status** (⬜/🟡/✅/⏭️) and the suggested order:
1. `working-preferences.md` (how you work — most important) 2. `bio.md` 3. `case-history.md`
4. `objectives.md` 5. `notion-sync.md` (optional) 6. current case (`/newcase`).

Then ask the **first question as a selectable choice** (use the AskUserQuestion tool so the
user clicks an option, don't make them type). Offer options like:
- **"Start at the top (recommended)"** — go in the suggested order.
- **"Paste my CV first"** — fast-fill `bio.md` + `case-history.md` from a résumé/LinkedIn.
- **"Let me pick a file"** — then ask which one.
(The user can always pick a specific file; "Other" lets them say so.)

## STEP 3 — The template-completion loop (repeat for EACH file)
For the chosen file (then the next, in order):
1. **Read the template** and enumerate its fields (`_(…)_` placeholders + table cells) —
   that's your checklist.
2. **Ask in grouped batches**, not one field per turn — cluster related fields into one
   question with a quick example. Invite a brain-dump.
3. **Map to fields; follow up on blanks.** For any field still empty, ask ONE targeted
   follow-up. Keep going until every field is filled or the user says "skip".
4. **Write the file**, then show it back for correction — never a raw dump, never a draft
   presented as final.
5. **Update `brain/setup-progress.md`** (mark the file ✅ done / 🟡 partial with the gaps /
   ⏭️ skipped, and stamp "Last updated"). Then move to the next file.

### Pacing rules (this is where the old setup failed)
- **Batch, never dribble** (don't ask name, then level, then office in three turns).
- **Infer before asking** — you have the work email and today's date; assume firm = BCG
  unless told. Never ask what you can infer.
- **Thorough but warm** — push for completeness, but let the user skip.

## Per-file guidance
- **working-preferences.md** — start with identity in ONE batch (full name · role +
  level/tenure · office · primary practices · sector focus · typical client profile · does
  the team use Claude / outputs shared); also write identity into `bio.md` + replace the
  `CLAUDE.md` placeholders. Then complete the rest: peak hours / protected time / slower
  period; output style; tool stack (→ Output-standards table); delivery ritual; when to
  push back; language; tone; what to never explain; hard "never do X"; stakeholder comms;
  recurring reminders; standing commitments.
- **bio.md** — offer the fast path FIRST: "paste your CV/LinkedIn (or a file path) and I'll
  draft this + your case history; you correct." Fill professional background, academic,
  leadership, skills & languages, live priorities (e.g. MBA), personal, and "Maestro
  context" (what you're fluent in).
- **case-history.md** — one entry per past case (client-or-confidential · type · sector ·
  year · role · summary · key skills · relevance) + summary table + patterns/strengths.
- **objectives.md** — offer `/feedback` with their latest feedback/review, or capture 2–4
  live objectives with what-good-looks-like + a practice cue.
- **notion-sync.md** — only if they use Notion: probe their DBs and fill the config; else ⏭️.

## STEP 4 — If they stop
That's fine — `brain/setup-progress.md` already records where they left off. Tell them
they can resume anytime by running `/setup` again (you'll pick up the ⬜/🟡 items), and that
Maestro will remind them at session start until it's complete.

## STEP 5 — Finish (when files are done or they stop)
Recap the progress table (✅/🟡/⏭️), then the next move: enable **Microsoft 365** (Claude
prompts on first brief) and **`/newcase <deck>`** for the current case; then **open a fresh
chat and run `/morning` — you're live.**

User's optional context: $ARGUMENTS
