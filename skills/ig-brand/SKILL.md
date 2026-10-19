---
name: ig-brand
description: >-
  Create or update the Instagram brand context file that every other ig skill
  reads - offer, audience, positioning, objections, customer language, voice,
  proof, goals, paid-ads settings and a Learnings table. Use when the user says
  "set up my brand", "positioning", "who is my audience", "describe my
  business", "ICP", "brand voice", "tone of voice", "niche", "what have we
  learned", "log this learning", "update my context", or is starting a new
  account or client. Run this first before the other ig skills. Writes
  ~/.claude/instagram/brand.md.
metadata:
  version: 3.0.0
---

# ig-brand

You create and maintain the account's **brand context**: the foundational
facts the other `ig-*` skills read, so the user does not repeat themselves in
every session. It is stored at `~/.claude/instagram/brand.md`. The voice has
its own file, `~/.claude/instagram/voice.md`, which `/ig-reel` and `/ig-human`
read.

Strong positioning is the highest-leverage Instagram work. A sharp niche and a
clear promise do more than any hook.

## Workflow

### Step 1: Check for existing context

Read `~/.claude/instagram/brand.md` if it exists.

**If it exists:** summarize what is captured, including the **Document
version** and the last few **Changelog** entries. Ask which sections to update
and gather information only for those. On any substantive save, bump the
version and add a changelog entry (Step 4).

**If it does not exist, offer two routes:**

1. **Auto-draft from what exists (recommended).** Ask for the handle or for
   pasted material: bio, last 10 to 20 captions, pinned posts, Highlights,
   link-in-bio page, the website, a testimonial or two, and `log.md` if it
   exists. Draft all sections, then ask what is wrong or missing.
2. **Start from scratch.** Walk through each section conversationally, one at
   a time.

### Step 2: Gather information

Do not dump all questions at once. For each section: explain what you are
capturing, ask, confirm, move on. Push for **verbatim customer language**.
Exact phrases beat polished descriptions because they are how the audience
actually thinks and speaks.

Never invent proof, results, testimonials or credentials. Mark unknowns as
unknown.

## Sections to capture

### 1. Account and offer
- Handle and account type (creator, local business, ecommerce, service, coach, agency client)
- One-line description of what is sold
- Category: the shelf people search on to find you
- Business model and price points
- What happens after someone is interested (DM, link, booking, shop)

### 2. Audience
- Who it is for, specifically (not "everyone")
- Where they are in life or business
- Primary problem or desire
- Jobs to be done: 2 to 3 things they hire you for
- Where they spend time on Instagram (Reels, Stories, DMs, search)

### 3. Problems and pain points
- The challenge before they found you
- Why current solutions fall short
- What it costs them (time, money, confidence)
- The emotional tension

### 4. Competitive landscape
- **Direct:** same solution, same problem
- **Secondary:** different solution, same problem
- **Indirect:** a conflicting approach, including doing nothing
- Three accounts they already follow that you compete for attention with
- How each falls short

### 5. Positioning and differentiation
- Key differentiators the alternatives lack
- How you solve it differently and why that is better
- Why customers choose you
- The positioning line: for [who], who [problem], [account] is [category] that [promise], unlike [alternative]

### 6. Objections and anti-audience
- Top 3 objections heard in DMs and comments, and the answer
- Who is not a good fit

### 7. Switching dynamics
- **Push:** frustrations with the current approach
- **Pull:** what attracts them to you
- **Habit:** what keeps them where they are
- **Anxiety:** what worries them about switching

### 8. Customer language
- How they describe the problem (verbatim, from comments, DMs, reviews)
- How they describe you (verbatim)
- Words to use and words to avoid
- Glossary of niche terms

### 9. Voice
A short summary lives in `brand.md`. The full profile lives in `voice.md`. Build
it from real posts and the user's own writing, not from adjectives picked in a
meeting. Method, examples and tone-by-context in
[references/brand-voice.md](references/brand-voice.md).

### 10. Content pillars
- 3 to 4 pillars, the job each does (reach, trust, conversion)
- Signature series, if any
- Topics that are off limits

### 11. Proof points
- Results with numbers and sample size
- Notable customers, collaborations, features, press
- Testimonial snippets with permission
- Value themes and the evidence for each

### 12. Goals
- Primary business goal and deadline
- Key conversion action (what you want people to do)
- Current metrics: followers, median reach, saves, DMs, link taps, revenue

### 13. Paid ads (optional, only if they run ads)
`/ig-ads` and `/ig-ad-creative` read this.
- Margin reality: target CPA or ROAS, and the hard floor
- Budget and acceptable daily variance
- Conversion truth: which actions count, what each is worth, known tracking weaknesses, what a good lead is
- Campaign naming convention and what each campaign is for
- What the agent may do (read, compare, flag, draft, recommend) and may not do without approval (change budgets, pause, launch, edit tracking, publish ads)

### 14. Learnings
Starts empty. Fills as work ships (see below).

## Step 3: Create the document

After gathering, write `~/.claude/instagram/brand.md`:

```markdown
# Instagram Brand Context

**Document version:** v1
**Last updated:** [date]

## Account and Offer
**Handle:**
**Account type:**
**One-liner:**
**Category:**
**Business model and price:**
**Next step after interest:**

## Audience
**Who it is for:**
**Primary problem or desire:**
**Jobs to be done:**
-
**Where they spend time:**

## Problems and Pain Points
**Core problem:**
**Why alternatives fall short:**
-
**What it costs them:**
**Emotional tension:**

## Competitive Landscape
**Direct:** [name] - falls short because...
**Secondary:** [approach] - falls short because...
**Indirect:** [alternative] - falls short because...

## Positioning
**Differentiators:**
-
**How we do it differently:**
**Why customers choose us:**
**Positioning line:**

## Objections
| Objection | Response |
|-----------|----------|
| | |

**Not a fit:**

## Switching Dynamics
**Push:**
**Pull:**
**Habit:**
**Anxiety:**

## Customer Language
**About the problem:**
- "[verbatim]"
**About us:**
- "[verbatim]"
**Words to use:**
**Words to avoid:**
**Glossary:**

## Voice (summary)
3 to 5 attributes. Full profile in voice.md.
| Attribute | Means | Doesn't mean | Example line |
|-----------|-------|--------------|--------------|
| | | | |

## Content Pillars
| Pillar | Job | Example |
|--------|-----|---------|
| | | |
**Signature series:**

## Proof Points
**Metrics:**
**Customers and collaborations:**
**Testimonials:**
> "[quote]" - [who]

## Goals
**Business goal:**
**Conversion action:**
**Current metrics:**

## Paid Ads (optional)
**Target CPA / ROAS:**
**Hard floor:**
**Monthly budget and daily variance:**
**Conversions that count:**
| Action | Means | Value | Feeds bidding? |
|--------|-------|-------|----------------|
| | | | |
**Known tracking weaknesses:**
**Good lead vs form fill:**
**Campaigns:** [name] - [what it is for]
**Agent may:** read, compare, flag, draft, recommend
**Agent may not (without approval):** change budgets, pause or launch, edit tracking, publish ads

## Learnings
*Decisions and tested lessons. Newest first. About 20 active entries.*
| Date | Learning | Evidence | Applies to | Status |
|------|----------|----------|------------|--------|
| | | | | |

## Changelog
*Newest first. One line per revision: what changed and why.*
- v1 ([date]) - Initial context.
```

## Step 4: Confirm, version and save

- Show the document and ask if anything needs adjusting.
- **New document:** `Document version: v1` and one Changelog entry.
- **Update:** increment the version, update `Last updated`, and prepend a Changelog entry naming the sections touched and why. Never rewrite past entries. Examples:
  - `- v3 (2026-09-16) - Narrowed from "fitness coach" to "postnatal strength coach"; added anti-audience.`
  - `- v2 (2026-06-02) - Rewrote objections after 20 DM conversations; added competitor account.`
- A typo-only fix does not bump the version.
- Save to `~/.claude/instagram/brand.md`. Create the folder if needed.
- If a real repositioning happened, say so plainly. Downstream skills will now generate against the new context.
- Tell the user: "The other ig skills now read this automatically. Run `/ig-brand` any time to update it."

## Voice file

If `~/.claude/instagram/voice.md` does not exist, build it from three to five of
the user's own Reels, captions and DMs, using the method in
`references/brand-voice.md`. `/ig-reel` expects: how they talk on camera, what
they never say, who they are talking to. Confirm with the user. Voice is a
choice, not an inference.

## Maintaining Learnings

The Changelog records how the document changed. **Learnings** records what the
account found out by shipping: which hooks won, which offers flopped, which
decisions were made and why. Drafting skills (`/ig-reel`, `/ig-caption`,
`/ig-ad-creative`, `/ig-plan`) read it before writing.

**Entry format**, one row per learning:
- **Learning:** one sentence specific enough to change a draft. "Reels that open on the result beat Reels that open on the question" works. "Be clearer" does not.
- **Evidence:** the test or source, with the number and sample size. "6 Reels each, median reach 2.1x, 3 weeks."
- **Applies to:** formats, audiences or skills it affects.
- **Status:** `active`, `watch` (one data point, worth retesting) or `retired`.

**What earns a place:**
- A test that reached its planned sample, or the same pattern across two or more campaigns
- A decision the user made with a reason (a niche cut, a format dropped) that future drafts must respect
- A correction the user gave more than once ("never call them clients, say members")

**What does not:** single-run anecdotes (log as `watch` or leave out), task notes, and anything that belongs elsewhere. A new objection goes in Objections. A new customer phrase goes in Customer Language.

**Retire** an entry when a later test contradicts it, the offer or audience
changed, or it has not been relevant for two quarters. Mark it `retired` with
the reason rather than deleting it, so nobody retests a settled question.
Archive retired rows once the table passes about 20 active rows.

**Who writes it:** any skill that finishes a test, campaign or post-mortem may
propose a row. Show it to the user and add it on approval, with a version bump
and a Changelog line. Scheduled loops do this through their session-end step
(see `/ig-loops`).

## Tips

- **Be specific.** Ask "What is the number one frustration that brings them to you?" not "What problem do they solve?"
- **Capture exact words.** Comments and DMs are the best source.
- **Ask for examples.** "Can you give me an example?" unlocks better answers.
- **Validate as you go.** Summarize each section before moving on.
- **Skip what does not apply.** Not every account needs Paid Ads.
- **No em dashes** in anything you write into the file.

## Related skills

- `/ig-profile`: turn the positioning into a bio, pins and Highlights
- `/ig-growth-plan`: build the plan on this context
- `/ig-council`: debate the positioning before committing
- `/ig-reel`, `/ig-caption`, `/ig-human`: read the voice
- `/ig-ads`, `/ig-ad-creative`: read the paid-ads section
- `/ig-psychology`: the principles behind the offer and proof
