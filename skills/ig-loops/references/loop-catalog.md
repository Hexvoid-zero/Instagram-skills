# Instagram Loop Catalog

22 loops. Each is a complete spec using the nine-part anatomy in `SKILL.md`.
Pick the closest, tune it to the account, and confirm the human checkpoint.
State files live in `~/.claude/instagram/loops/<loop>.json`.

## Contents

- Planning: 1 weekly plan, 2 swipe refresh, 3 monthly post-mortem, 4 weekly review
- Content: 5 top-post repurpose, 6 hook bank refill, 7 series tracker, 8 daily creative drop
- Community: 9 comment sweep, 10 DM triage, 11 pillar-account commenting, 12 lead follow-up
- Growth and paid: 13 early-performance check, 14 boost candidate, 15 ad fatigue, 16 weekly ads check, 17 retargeting hygiene
- Brand and ops: 18 profile rot check, 19 niche watch, 20 collab pipeline, 21 crisis watch, 22 campaign post-mortem

---

## Planning

### 1. The weekly plan loop
- **Check cadence**: Weekly, Sunday evening or Monday morning
- **Acts when**: Always. This is the heartbeat.
- **Purpose**: A concrete week: what posts, which formats, which days, who to engage with.
- **Skills used**: `ig-plan`, `ig-viral`, `ig-audit`
- **Loop body**:
  1. Read `log.md`, last week's results and `brand.md` goals.
  2. Pull fresh patterns from `swipe.md`.
  3. Draft the week with `/ig-plan`: slots, formats, hooks, engagement targets.
  4. Write it to `plan.md`.
- **Self-check**: Does the plan fit the stated weekly hours? Does it repeat a format flagged as a flop in Learnings?
- **State / idempotency**: Last planned week; do not replan the same week unless asked.
- **Stop / bail-out**: If `log.md` has no new entries for two weeks, ask the user to log posts before planning again.
- **Output**: `plan.md` and a one-screen summary.

### 2. The swipe-file refresh loop
- **Check cadence**: Weekly or fortnightly
- **Acts when**: At least 5 new outlier posts are found in the niche.
- **Purpose**: Keep the hook and format swipe file current.
- **Skills used**: `ig-viral`
- **Loop body**: Scan the seed accounts and hashtags; rank by lift over each account's own median; name the hook formula; append to `swipe.md`; drop entries older than 90 days.
- **Self-check**: Is the outlier a reach fluke (one-off, paid, giveaway)? Skip those.
- **State**: Post URLs already added.
- **Stop / bail-out**: If the scraping source fails, report "stale" and do not fabricate entries.
- **Output**: Updated `swipe.md` plus the three best new formats.

### 3. The monthly post-mortem loop
- **Check cadence**: Monthly
- **Acts when**: At least 10 posts have been logged in the window.
- **Purpose**: Learn what to make more and less of.
- **Skills used**: `ig-audit`, `ig-brand`
- **Loop body**: Read the month in `log.md`; run `/ig-audit`; rank by save rate, share rate and reach vs median; name patterns; propose Learnings rows.
- **Self-check**: Sample size, seasonality, one post skewing the median, paid boosts mixed in.
- **State**: Month already reviewed.
- **Stop / bail-out**: Under 10 posts, run a shorter review and say the sample is thin.
- **Output**: A one-page post-mortem and proposed Learnings rows for approval.

### 4. The weekly review loop
- **Check cadence**: Weekly
- **Acts when**: Always.
- **Purpose**: A single view of the account: reach, followers, saves, DMs, link clicks, paid if any.
- **Skills used**: `ig-audit`, `ig-ads`
- **Loop body**: Pull the week's numbers; compare to the 4-week average; flag movers; route each to the loop that owns it.
- **Self-check**: Is a drop a real change or a missing export?
- **State**: Last review date and baseline.
- **Stop / bail-out**: Missing data is reported as missing.
- **Output**: A short report with the next action per mover.

## Content

### 5. The top-post repurpose loop
- **Check cadence**: Weekly
- **Acts when**: A post beats the median by the agreed threshold and has not been repurposed.
- **Purpose**: Get more from what already works.
- **Skills used**: `ig-repurpose`, `ig-carousel`, `ig-story`
- **Loop body**: Find qualifying posts; propose a carousel, Story sequence and a Reel reply; stage drafts.
- **Self-check**: Is it still current? Was it a paid boost?
- **State**: Repurposed post IDs.
- **Stop / bail-out**: Max two repurposes per source post.
- **Output**: Staged drafts in the weekly plan.

### 6. The hook bank refill loop
- **Check cadence**: Fortnightly
- **Acts when**: Unused hooks drop below 15.
- **Purpose**: Never start a Reel from a blank page.
- **Skills used**: `ig-reel`, `ig-viral`, `ig-human`
- **Loop body**: Generate hooks from comments, DMs, swipe formulas and the brand voice; remove duplicates; run through `ig-human`.
- **Self-check**: Does each hook map to a topic the account can credibly cover?
- **State**: Used and unused hook IDs.
- **Stop / bail-out**: Cap at 40 hooks in the bank.
- **Output**: `hooks.md` in the loop folder.

### 7. The series tracker loop
- **Check cadence**: Weekly
- **Acts when**: A named series has run 3 episodes.
- **Purpose**: Decide whether a series continues, changes or ends.
- **Skills used**: `ig-audit`, `ig-plan`
- **Loop body**: Compare episodes to the account median; check follower conversion per episode; recommend continue, tweak or stop.
- **Self-check**: Three data points are a trend only if the format held constant.
- **State**: Episode list per series.
- **Stop / bail-out**: Never kill a series on fewer than 3 episodes.
- **Output**: A keep, tweak or stop call with evidence.

### 8. The daily creative drop loop
- **Check cadence**: Daily, weekdays
- **Acts when**: Static ad inputs exist and the creative backlog is under target.
- **Purpose**: Steady supply of grounded ad concepts.
- **Skills used**: `ig-ad-creative`, `ig-human`
- **Loop body**: Pick the next template and angle; draft from the grounded inputs; cite sources; validate specs; stage.
- **Self-check**: Every concept cites a real review, ad or comment.
- **State**: Templates and angles used this cycle.
- **Stop / bail-out**: If inputs are stale, stop and ask for fresh ones.
- **Output**: A dated batch folder and index.

## Community

### 9. The comment sweep loop
- **Check cadence**: Daily
- **Acts when**: There are new comments worth answering.
- **Purpose**: Keep reply speed up and turn comments into conversations.
- **Skills used**: `ig-reply`, `ig-human`
- **Loop body**: Pull new comments; sort into answer now, answer later, ignore, escalate; draft replies in the account voice.
- **Self-check**: Is the commenter a lead, a critic or a bot?
- **State**: Comment IDs handled.
- **Stop / bail-out**: Replies are staged for approval. Critics and sensitive topics always escalate.
- **Output**: A reply queue.

### 10. The DM triage loop
- **Check cadence**: Daily
- **Acts when**: New threads exist.
- **Purpose**: Never let a warm lead go cold.
- **Skills used**: `ig-dm`, `ig-human`
- **Loop body**: Sort threads (lead, support, collab, spam); draft replies; flag anyone waiting over 24 hours.
- **Self-check**: Is a keyword-trigger reply still the right message for this person?
- **State**: Thread IDs and last-contacted timestamps.
- **Stop / bail-out**: Staged only. No auto-send.
- **Output**: A triage list with drafts.

### 11. The pillar-account commenting loop
- **Check cadence**: Daily
- **Acts when**: A target account posts something relevant within the last few hours.
- **Purpose**: Earn visibility from the right audience.
- **Skills used**: `ig-comment`
- **Loop body**: Check the ten target accounts; draft one specific, useful comment for each fresh post.
- **Self-check**: Is the comment adding something, or just praise?
- **State**: Posts commented on.
- **Stop / bail-out**: Stage for the human to post. Max 10 a day.
- **Output**: A comment list.

### 12. The lead follow-up loop
- **Check cadence**: Daily
- **Acts when**: A lead has not replied in the cooldown window.
- **Purpose**: A polite second touch that does not nag.
- **Skills used**: `ig-dm`
- **Loop body**: Find silent leads; draft one helpful follow-up with a new reason to reply.
- **Self-check**: Did they ask to stop? Check the suppression list.
- **State**: Cooldowns and attempt counters per thread.
- **Stop / bail-out**: Two follow-ups max, then stop.
- **Output**: Staged follow-ups.

## Growth and paid

### 13. The early-performance check loop
- **Check cadence**: At 24 and 72 hours after each post
- **Acts when**: A post is clearly above or below the median.
- **Purpose**: React while distribution is live.
- **Skills used**: `ig-audit`, `ig-story`, `ig-reply`
- **Loop body**: Pull early reach and shares; if above median, queue Story amplification and fast comment replies; if below, log the hypothesis.
- **Self-check**: Compare to posts at the same hour and format.
- **State**: Post IDs checked.
- **Stop / bail-out**: Do not edit or delete the post on a single data point.
- **Output**: A short action list.

### 14. The boost candidate loop
- **Check cadence**: Weekly
- **Acts when**: A post beats the median by a large margin and has commercial relevance.
- **Purpose**: Put budget behind proven organic content.
- **Skills used**: `ig-ads`
- **Loop body**: List candidates; propose objective, audience, budget and duration; stage for approval.
- **Self-check**: Is the destination ready and tracked?
- **State**: Posts already boosted.
- **Stop / bail-out**: Spend is always gated.
- **Output**: A boost proposal.

### 15. The ad fatigue loop
- **Check cadence**: Every 2 to 3 days
- **Acts when**: Frequency rises and CTR or hook rate falls past the agreed drift.
- **Purpose**: Refresh creative before efficiency collapses.
- **Skills used**: `ig-ads`, `ig-ad-creative`
- **Loop body**: Pull creative-level metrics; flag fatigued ads; draft replacement variants from winning angles.
- **Self-check**: Is it fatigue, or seasonality or a learning phase reset?
- **State**: Ads flagged and refreshed.
- **Stop / bail-out**: Never pause a winner without a staged replacement.
- **Output**: A fatigue report and staged variants.

### 16. The weekly ads check loop
- **Check cadence**: Weekly
- **Acts when**: Spend is above the minimum for a meaningful read.
- **Purpose**: Run the Meta operating check.
- **Skills used**: `ig-ads`
- **Loop body**: Apply the decision system in `/ig-ads` references; produce scale, hold, kill calls.
- **Self-check**: Tracking intact; enough conversions.
- **State**: Last decisions per ad set.
- **Stop / bail-out**: Anomalies in spend or revenue are flagged, not corrected.
- **Output**: A dated report.

### 17. The retargeting hygiene loop
- **Check cadence**: Monthly
- **Acts when**: Audience sizes or exclusions look off.
- **Purpose**: Keep retargeting clean.
- **Skills used**: `ig-ads`
- **Loop body**: Check audience sizes, windows and buyer exclusions; refresh creative for the four-ad sequence.
- **Self-check**: Is the audience large enough to spend into?
- **State**: Last audit.
- **Stop / bail-out**: Changes are staged.
- **Output**: A short audit.

## Brand and ops

### 18. The profile rot check loop
- **Check cadence**: Monthly
- **Acts when**: The bio, pinned posts, Highlights or link are out of date.
- **Purpose**: Keep the conversion surface current.
- **Skills used**: `ig-profile`
- **Loop body**: Review against `brand.md`; flag a stale offer, dead link, outdated pin.
- **Self-check**: Does the profile still match the current goal?
- **State**: Last review.
- **Stop / bail-out**: Changes are suggested, not applied.
- **Output**: A fix list.

### 19. The niche watch loop
- **Check cadence**: Weekly
- **Acts when**: A competitor or peer changes format, offer or pricing visibly.
- **Purpose**: Notice shifts early.
- **Skills used**: `ig-viral`
- **Loop body**: Review the watch list; summarize changes; flag threats and openings.
- **Self-check**: Is it a one-off or a pattern?
- **State**: Last snapshot per account.
- **Stop / bail-out**: Observation only. No copying.
- **Output**: A short brief.

### 20. The collab pipeline loop
- **Check cadence**: Weekly
- **Acts when**: A prospect has no next step or a live collab is due.
- **Purpose**: Keep collabs moving.
- **Skills used**: `ig-dm`, `ig-pr`
- **Loop body**: List prospects and stage; draft outreach or follow-ups; track deliverables and dates.
- **Self-check**: Audience overlap and brand fit.
- **State**: Stage and last contact per prospect.
- **Stop / bail-out**: Outreach is staged. Contracts go to a human.
- **Output**: A pipeline table.

### 21. The crisis watch loop
- **Check cadence**: Daily, or hourly during an incident
- **Acts when**: Negative comments, tags or reposts spike.
- **Purpose**: Catch a problem while it is small.
- **Skills used**: `ig-reply`, `ig-pr`
- **Loop body**: Scan mentions and comment sentiment; classify; draft holding statements.
- **Self-check**: Is the volume real or a few loud accounts?
- **State**: Incident ID and status.
- **Stop / bail-out**: Always escalate to a human. Never auto-respond.
- **Output**: An alert with options.

### 22. The campaign post-mortem loop
- **Check cadence**: After each campaign or launch
- **Acts when**: A campaign ends.
- **Purpose**: Capture what held.
- **Skills used**: `ig-audit`, `ig-ads`, `ig-brand`
- **Loop body**: Compare results to the goal; document what worked; propose Learnings rows.
- **Self-check**: Attribution limits stated.
- **State**: Campaigns reviewed.
- **Stop / bail-out**: One-off results stay in the log.
- **Output**: A short write-up and proposed Learnings.

---

## Adapting and authoring loops

Start from the closest loop. Change the cadence to match the account's volume, tighten **acts when** until most runs do nothing, and make the stop condition specific. For a brand-new loop, use `loop-template.md`.
