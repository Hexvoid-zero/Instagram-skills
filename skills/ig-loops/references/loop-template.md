# Loop Template

A copy-paste template for authoring your own Instagram loop. Fill every one of the nine parts - a loop missing its **state/idempotency**, **self-check**, or **stop/bail-out** isn't a system, it's a way to do the wrong thing on a schedule.

Before you start, sanity-check that this *should* be a loop at all (see "When NOT to loop" in `SKILL.md`): it's recurring, signal-driven, and doesn't require human judgment to set strategy or creative direction each run.

---

## Blank template (copy this)

```markdown
### The <name> loop
- **Check cadence**: <how often it looks - match to how fast the signal changes, not how often you'd like an update>
- **Acts when**: <the action condition - what must be true to actually DO something vs. just check and skip. Most runs should skip.>
- **Purpose**: <the ONE outcome this loop exists to move>
- **Skills used**: <which marketing skills the loop orchestrates each run>
- **Loop body**:
  1. <step - usually: pull data / diff vs. last run>
  2. <step - identify what, if anything, crossed the action condition>
  3. <step - draft or stage the response>
- **Self-check**: <the verification done BEFORE acting - is the signal real vs. noise/seasonality/tracking bug? Is the sample big enough to be significant?>
- **State / idempotency**: <what it remembers between runs - last-run marker, dedupe key, cooldown window, "already handled" set - so it doesn't double-act or re-nag the same people>
- **Stop / bail-out**: <when it skips, halts, escalates to a human, or disables itself - plus what it does on error. Include a human checkpoint before anything that spends money or publishes.>
- **Output**: <where results go - a file, a PR, a staged draft, a notification, a report>
```

---

## Fill-in prompts (answer these, in order)

1. **What outcome does this protect or grow?** (reach, saves, followers, DMs, ad efficiency, response time) → *Purpose*
2. **How fast does that signal actually change?** (hours / days / weeks / months) → *Check cadence*
3. **What has to be true before it's worth acting?** (a threshold crossed, a new item appeared, a regression vs. baseline) → *Acts when*
4. **What data does it read and what does it produce each run?** → *Loop body* + *Output*
5. **What would make it act on a false signal?** (noise, seasonality, a tracking break, too-small a sample) → *Self-check*
6. **What must it remember so it doesn't repeat itself?** (dedupe key, cooldown, last-run marker) → *State / idempotency*
7. **When should it stop, skip, or hand off to a human?** (no action needed, error, spend/publish decision, N failed attempts) → *Stop / bail-out*

If you can't answer 5, 6, and 7 concretely, the loop isn't ready to run.

---

## Worked example (blank → filled)

Say you coach freelancers, and warm leads keep going silent after their first DM.

```markdown
### The silent-lead follow-up loop
- **Check cadence**: Daily
- **Acts when**: A lead replied once, then went quiet for 3 days, and is not already in a follow-up.
- **Purpose**: Turn warm DM conversations into booked calls without nagging.
- **Skills used**: `ig-dm`, `ig-human`
- **Loop body**:
  1. Pull DM threads from the last 14 days with their last-message time.
  2. Filter to quiet leads outside the cooldown window.
  3. Draft one helpful follow-up per lead with a new reason to reply (a resource, a question, a time slot).
- **Self-check**: Did the lead say no or ask to stop? Did the thread move to another channel?
- **State / idempotency**: Track attempts and cooldown per thread ID; one follow-up per 5 days; suppress anyone who replied.
- **Stop / bail-out**: After 2 follow-ups with no reply, stop and tag the thread cold. Drafts are staged, never auto-sent.
- **Output**: A staged list of follow-ups and a daily count of revived threads.
```

Notice what makes it safe: the **self-check** guards against messaging someone who already said no, the **state** stops it re-nagging, and the **stop** caps attempts and hands off instead of looping forever.

---

## Ship checklist

Before you schedule a new loop, confirm:

- [ ] All nine parts are filled - especially self-check, state, and stop.
- [ ] Cadence matches signal speed (you're not checking daily for a weekly-moving signal).
- [ ] It's designed so **most runs do nothing** - it acts only on a real condition.
- [ ] Anything that **spends money or publishes** has a human checkpoint (unless caps + an allowlist are explicitly authorized).
- [ ] State prevents double-acting and re-nagging the same people.
- [ ] There's an error path (stale data → report "stale," don't fabricate movement) and a manual off switch.
- [ ] For scheduling mechanics, see the "Scheduling a loop" section in `SKILL.md`.

Once it runs, give it a few cycles and ask the "is this a vanity loop?" question: if nobody acts on the output, delete it.
