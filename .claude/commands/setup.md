---
description: First-run onboarding — walks template-by-template and asks targeted questions to fill EVERY field of each brain template as completely as possible
---

You are running the **guided first-time setup**. Goal: take a brand-new user from a fresh
template to a live, *fully-populated* system. The method is a **template-completion loop**:
go through each brain template that needs filling, and drive questions until every field is
filled (or explicitly skipped) — then move to the next template.

## The core method — repeat for EACH template below
For every target file:
1. **Read the template** and enumerate its sections/fields (the `_(…)_` placeholders and
   table cells). That list is your checklist for this file.
2. **Ask in grouped batches**, not one field per turn — cluster related fields into one
   question, with a quick example of the kind of answer that helps. Invite a brain-dump.
3. **Map the answer to the fields.** For any field still empty, ask ONE targeted follow-up
   ("still missing: peak hours and your slower period — when are those?"). Keep going until
   every field is filled or the user says "skip" / "good enough".
4. **Write the file**, then show it back for correction — never leave a raw dump, never
   present a draft as final.
5. **Confirm and move to the next template.**
Track progress so the user can stop and re-run `/setup` later (resumable) — you only do
what's still blank.

## Pacing & style (this is where the old setup failed)
- **Batch, never dribble.** Don't ask name, then level, then office in three turns — ask a
  whole block at once.
- **Infer before asking.** You already have the work email (from the system) and today's
  date; assume the firm is BCG unless told. Never ask what you can infer.
- **Thorough, not interrogating.** Push for completeness (follow up on blanks) but stay
  warm and quick; let the user say "skip" on anything.
- Set expectations up front: "I'll walk you through ~5 files to fill in — identity & how
  you work, your background, your case history, development goals, and tasks. I'll ask in
  batches and we'll fill each one out properly. Say 'skip' anytime."

## 0. Diagnose first
Scan for first-run signals (placeholders `{{OWNER}}`/`{{SEU_NOME_COMPLETO}}`/`{{SEU_EMAIL}}`;
profile/objectives still template; `clients|projects/` only `_template.md`; `notion-sync.md`
unconfirmed; empty `brain/daily/`). Show a compact ✅/⬜ checklist of the files to fill, then
start the loop. If everything's done, point them to `/morning` instead.

## The templates to complete, in order

### A. `brain/profile/working-preferences.md` (most important — read every session)
Start with identity (ONE batch: full name · role + level/tenure · office · primary
practices · sector focus · typical client profile · does the team use Claude / are outputs
shared) — pre-fill email and also write these into `bio.md` Identity + replace the
`CLAUDE.md` placeholders. Then complete the rest of the file, batched: peak hours +
protected time + slower period; output style (answer-first? MECE? bullets vs prose?
high-level-then-drill?); tool stack (analysis/dashboards/models/slides/docs → the
Output-standards table); delivery ritual; when to push back; default language; tone; what
you never need explained (areas of fluency); any hard "never do X"; stakeholder-comms
register; recurring reminders (timesheets/expenses/backlog); standing commitments. Follow
up until each section has content.

### B. `brain/profile/bio.md`
**Offer the fast path first:** "Paste your CV/résumé text or LinkedIn About+Experience (or a
file path) and I'll draft this — you just correct." Parse into every section: professional
background (roles + dates + highlights), academic, leadership/activities, skills &
languages, live priorities (e.g. MBA), personal interests / what energizes you, and the
"Maestro context" (what to assume you're fluent in). If they'd rather talk, ask those
sections in 2-3 batched questions. Fill every field; show back.

### C. `brain/profile/case-history.md`
If a CV/deck was shared, seed entries from it. Then complete: one entry per past case
(client-or-confidential · type · sector · year · role · summary · key skills · relevance),
the summary table, and patterns/strengths (depth areas · quantitative/technical · sectors
covered · potential gaps). Ask case-by-case; aim for their last several engagements.

### D. `brain/development/objectives.md`
Best source = formal feedback: offer to run `/feedback` with their latest project feedback
and last review. Otherwise capture 2-4 live objectives directly, each with
what-good-looks-like + a daily practice cue. (Drives the daily nudge + Friday retro.)

### E. `brain/tasks/notion-sync.md` (only if they use Notion)
If they keep tasks in Notion, probe their databases and fill the config (database + data
source ID + property mapping); else mark it skipped and note `backlog.md` is enough.

## Then: integrations & current case
- **Microsoft 365** — Claude will prompt to authenticate the first time the brief runs.
- **Current case** — offer `/newcase <proposal deck path>` to populate `clients/` +
  `projects/` and add a rich case-history entry.

## Finish
Recap each template as ✅ complete / 🟡 partial (name the gaps) / ⬜ skipped, then the next
move: **open a fresh chat and run `/morning` — you're live.** Remind them `/setup` is
resumable to finish any 🟡/⬜ later.

User's optional context: $ARGUMENTS
