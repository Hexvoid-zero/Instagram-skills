---
name: ig-loops
description: >-
  Set up recurring, repeatable Instagram workflows an agent runs on a cadence
  (weekly, daily, on a trigger) instead of one-off tasks. Use when the user says
  "Instagram loop", "recurring workflow", "automate my Instagram", "weekly
  Instagram review", "ad fatigue check", "run this every week", "comment sweep
  every day", "monthly content audit", "daily creative drop", "always-on
  Instagram", or wants to pick, adapt and schedule an ongoing routine that ties
  together the other ig skills.
metadata:
  version: 2.0.0
---

# ig-loops

You help set up **Instagram loops**: repeatable workflows an agent runs on a
cadence, each with a trigger, a bounded set of steps, a self-check and an
explicit stop condition. A loop turns a task you would otherwise do by hand,
and forget, into a system: the weekly plan, the comment sweep, the ad-fatigue
refresh, the monthly post-mortem.

`/ig-ideas` says what to try once. Loops say what to keep doing on a schedule,
and wire the other `ig-*` skills together to do it.

## Before starting

Read, if present, and ask only for what is missing:

- `~/.claude/instagram/brand.md` - goals, offer, audience, Learnings
- `~/.claude/instagram/plan.md` and `log.md` - the current week and what has
  shipped
- `~/.claude/instagram/loops/` - existing loop state files, so you do not build
  a second copy of a loop that already exists

Then:

1. **Clarify the job.** What outcome should the loop protect or grow? (reach,
   saves, followers, DMs, sales, ad efficiency, response time)
2. **Pick a loop** from `references/loop-catalog.md`, or adapt the closest one.
3. **Tune the cadence** to how fast the signal changes (rule below).
4. **Confirm the human checkpoint.** What the loop does alone and what it
   stages for approval. See `references/loop-guardrails.md`.
5. **Schedule it** (below).

Building more than one loop? `references/loop-orchestration.md` gives the
order to adopt them. Start with the weekly plan and a post-mortem. Do not
build them all at once.

## Anatomy of a loop

Every loop in the catalog has these nine parts. Fill all of them when you
author or adapt one. A loop without a stop condition, self-check or state
handling is a liability.

| Part | What it defines |
|------|-----------------|
| **Check cadence** | How often it looks. Match signal speed. |
| **Acts when** | What must be true to actually do something. Most runs should be "checked, nothing to do." |
| **Purpose** | The one outcome it moves. |
| **Skills used** | Which `ig-*` skills it orchestrates. |
| **Loop body** | The ordered steps each run. |
| **Self-check** | Verification before acting, so it does not act on noise, a holiday dip or a tracking bug. |
| **State / idempotency** | What it remembers between runs. See `references/loop-state.md`. |
| **Stop / bail-out** | When it skips, halts, escalates or disables itself, and what it does on error. |
| **Output** | Where results go: a file, a staged draft, a report, a notification. |

Split **check cadence** from **acts when**. A comment sweep may check daily but
only act when a new comment crosses the "worth answering" bar.

## The cadence rule

Match cadence to how fast the signal changes, not to how often you would like
an update.

| Signal | Realistic cadence | Why |
|--------|-------------------|-----|
| Reel performance vs the account median | Review at 48 to 72 hours, then weekly | Most distribution happens early, then tails |
| Weekly plan | Weekly | The unit of work |
| Comments and DMs | Daily | Reply windows close fast |
| Follower and reach trend | Weekly | Daily swings are noise |
| Ad fatigue, CPA drift | Every 2 to 3 days | Feedback is days, not hours |
| Hook and format swipe refresh | Weekly to fortnightly | The niche moves slowly enough |
| Profile and Highlights health | Monthly | Changes are rare |
| Content post-mortem | Monthly | Needs enough posts to be significant |
| Competitor and niche watch | Weekly | Shifts matter but are infrequent |

Over-frequent loops are the common failure. They create busywork and train you
to ignore the output.

## When not to loop

- **Strategy or creative direction is the real work.** Loops maintain and
  optimize. They do not set positioning or make brand calls.
- **The action publishes, replies or spends without review.** Auto-drafting is
  fine. Auto-posting, auto-replying and auto-shifting budget need a human check
  unless the user explicitly authorizes it with caps. See the guardrails.
- **The signal is too sparse.** A weekly engagement-rate loop on three posts
  measures noise.
- **It is a vanity loop.** If nobody acts on the output, delete it.

## Scheduling a loop

The loop body works in any agent. Scheduling depends on the environment:

- **Scheduled tasks.** If this session offers scheduled-task tools, create the
  loop as one, with a complete standalone prompt. Each run starts fresh, so the
  prompt must tell it to read the state file and the context files first.
- **Cron or another scheduler.** Wrap the body as a scheduled prompt.
- **Manual cadence.** For high-judgment loops, "run `/ig-plan` every Monday" is
  a perfectly good loop. The value is the repeatable body, not the automation.

Default to a fixed day and time for review-style loops. Use dynamic pacing for
loops that watch until a threshold is crossed.

## The catalog

`references/loop-catalog.md` holds 22 Instagram loops grouped by Planning,
Content, Community, Growth and Paid, Brand and Ops. Each is a complete,
adaptable spec. Pick the closest and tune it.

## Authoring a new loop

When nothing fits, use `references/loop-template.md`: a template with fill-in
prompts, a worked example and a ship checklist. If you cannot answer the
self-check, state and stop parts concretely, the loop is not ready.

## Anti-patterns

- No stop condition: runaway spend or endless churn.
- Same cadence for everything: most loops run too often.
- No self-check: acting on noise.
- Auto-publishing or auto-replying without a checkpoint. Instagram detects
  automation and brand risk is real.
- Ten loops at once. Start with one and prove it earns its keep.

## Banned vocabulary

Avoid "set it and forget it", "fully autonomous Instagram", "AI does
everything", "10x on autopilot", "growth hacking machine". Loops are
disciplined systems with checkpoints, not magic.

## Related skills

- `/ig-ideas`: one-off tactics. Loops operationalize the ones worth repeating.
- `/ig-plan`, `/ig-audit`, `/ig-viral`, `/ig-reply`, `/ig-comment`, `/ig-dm`,
  `/ig-profile`: the building blocks the loops orchestrate
- `/ig-ads`, `/ig-ad-creative`: the paid loops
- `/ig-brand`: the context file and Learnings table
- `/ig-human`: the final text pass
