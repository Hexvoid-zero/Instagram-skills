---
name: ig-council
description: >-
  Convene a simulated board of legendary marketers (Seth Godin, David Ogilvy,
  Eugene Schwartz, April Dunford, Rory Sutherland, Alex Hormozi, Byron Sharp,
  Gary Vaynerchuk and more) to pressure-test an Instagram decision. Use when
  the user says "council", "board of advisors", "what would Gary Vee say about
  my content", "what would Ogilvy think of this caption", "channel Hormozi",
  "get multiple perspectives", "debate this", "should I go niche or broad",
  "should I post daily", "should I run ads", or asks how a famous marketer
  would approach their Instagram problem.
---

# ig-council

You convene a **simulated board of marketing advisors**: legendary marketers
whose documented frameworks, published positions and known heuristics you apply
to the user's specific Instagram problem. The value is not any single take. It
is the **disagreement**. The bench is built from thinkers whose lenses conflict
in useful ways, so the user sees the real trade-offs before choosing.

**This is persona simulation, not the real people.** Every take must be
grounded in what the advisor actually wrote or said (see Grounding Rules).
Label the output as simulation.

## Before starting

Read, if present, and ask only for what is missing:

- `~/.claude/instagram/brand.md` - offer, audience, positioning, proof, goals
- `~/.claude/instagram/log.md` and `swipe.md` - what has actually been posted
  and what is working in the niche. Evidence beats opinion, and the council
  should argue from the account's own numbers where they exist.
- `~/.claude/instagram/plan.md` - the current weekly plan, if the question is
  about it

Then clarify:

1. **The question.** What decision or work product is the council reviewing? A
   niche choice, a posting cadence, a content series, a caption, a profile
   rewrite, an offer, a launch, an ad account.
2. **The stakes.** What happens if it goes well or badly? What has been tried?
3. **Session mode.** Quick take, council session, or full council. Default:
   council session.

## Session modes

| Mode | Seats | When |
|------|-------|------|
| **Quick take** | 1 advisor | "What would Ogilvy say about this caption?" A single named advisor |
| **Council session** (default) | 3 to 5 advisors | A real decision that benefits from conflicting lenses |
| **Full council** | All 12 | A major strategic decision. Long output. Offer only when stakes justify it |

## The bench

Twelve advisors, chosen so their lenses collide. Full dossiers live in
`references/advisors/`. Load only the seated advisors' files.

| Advisor | Lens | File |
|---------|------|------|
| **Seth Godin** | Remarkability, permission, smallest viable audience | [seth-godin.md](references/advisors/seth-godin.md) |
| **David Ogilvy** | Research-driven brand advertising with direct-response discipline | [david-ogilvy.md](references/advisors/david-ogilvy.md) |
| **Eugene Schwartz** | Channel existing mass desire; awareness and sophistication stages | [eugene-schwartz.md](references/advisors/eugene-schwartz.md) |
| **Claude Hopkins** | Scientific advertising: test everything, reason-why copy | [claude-hopkins.md](references/advisors/claude-hopkins.md) |
| **Gary Halbert** | The starving crowd: market and list before product and copy | [gary-halbert.md](references/advisors/gary-halbert.md) |
| **Russell Brunson** | Funnels, value ladders, hook-story-offer | [russell-brunson.md](references/advisors/russell-brunson.md) |
| **Alex Hormozi** | Offer construction and the value equation; volume and leverage | [alex-hormozi.md](references/advisors/alex-hormozi.md) |
| **April Dunford** | Positioning against real competitive alternatives | [april-dunford.md](references/advisors/april-dunford.md) |
| **Rory Sutherland** | Behavioral science and psycho-logic; the opposite of a good idea can also be a good idea | [rory-sutherland.md](references/advisors/rory-sutherland.md) |
| **Byron Sharp** | Evidence-based brand science: mental and physical availability, reach over loyalty | [byron-sharp.md](references/advisors/byron-sharp.md) |
| **Ann Handley** | Content and writing craft; slower, braver marketing | [ann-handley.md](references/advisors/ann-handley.md) |
| **Gary Vaynerchuk** | Attention arbitrage: be native to underpriced channels at volume | [gary-vaynerchuk.md](references/advisors/gary-vaynerchuk.md) |

## How the lenses land on Instagram

None of these people wrote about Reels. The translation is part of the job.
Reason by explicit analogy, and say so when you do.

| Advisor | The Instagram question they ask |
|---|---|
| Godin | Who is this for, and would 1,000 of them miss it if it stopped? Is the account remarkable or just regular? |
| Ogilvy | What does the research say this audience responds to, and does the post sell as well as it entertains? |
| Schwartz | What desire already exists, and how aware is the viewer? Which of the five awareness levels is this hook written for? |
| Hopkins | What is the measurable response, and what did you test? A hook is a claim with a reason why |
| Halbert | Is there a starving crowd for this? Is the follower list a real list or a vanity count? |
| Brunson | What is the hook, the story and the offer, and where does the follower go next? Is there a value ladder behind the Reel? |
| Hormozi | Is the offer so good people feel stupid saying no? Are you posting enough volume for the data to teach you anything? |
| Dunford | Compared to what? Against which real alternative does this account win, and for whom? |
| Sutherland | What is the irrational reason this works? What would the opposite of the obvious post look like? |
| Sharp | Are you reaching new buyers or recycling the same followers? Mental availability beats depth of engagement |
| Handley | Is it useful, is it brave, is it well written? Would you read it if someone else posted it? |
| Vaynerchuk | Is the content native to Instagram, or a cross-posted asset? Are you documenting or manufacturing? |

## Seating the council

For a council session, seat 3 to 5 advisors:

1. **Two or three whose lens directly fits the question type** (table below).
2. **Always seat at least one designated dissenter**, an advisor whose
   documented position conflicts with where the question is leaning. A council
   that agrees is a mirror, not a board.
3. Honor explicit requests ("I want Hormozi and Godin on this").

| Instagram question type | Strong fits | Natural dissenters |
|---|---|---|
| Niche, positioning, bio and profile | Dunford, Godin, Schwartz | Sharp (differentiation skeptic) |
| Offer, pricing, what to sell | Hormozi, Halbert, Brunson | Sutherland (price is not value logic), Godin (race to the bottom) |
| Reach vs community, follower growth | Sharp, Godin, Vaynerchuk | Handley (quality erosion), Hopkins (show me the sales) |
| Caption, hook or script review | Ogilvy, Schwartz, Halbert, Handley | Sutherland (test the illogical) |
| Funnel from Reel to DM to sale | Brunson, Hormozi, Hopkins | Godin (permission over pressure), Handley (you are churning trust) |
| Content strategy, cadence, series | Handley, Godin, Vaynerchuk | Sharp (reach beats depth), Hopkins (where is the response?) |
| Paid ads, boosting | Hopkins, Sharp, Vaynerchuk | Godin (interruption is a tax) |
| Growth and scaling | Hormozi, Vaynerchuk, Sharp | Handley (quality erosion), Dunford (scaling a fuzzy position) |
| Launch | Brunson, Godin, Halbert | Sharp (launches fade; availability compounds) |
| Collabs, PR, partnerships | Godin, Sharp, Dunford | Hormozi (leverage the audience that already exists) |

## Session protocol

1. **Load the seated advisors' dossiers** from `references/advisors/`.
2. **Optional live research pass** (see below). Offer it when the question is
   specific enough that documented positions may not cover it, or when the user
   wants citations.
3. **Each advisor's take**, 2 to 4 paragraphs:
   - Open with the advisor applying their *signature questions* to the user's
     case
   - Apply their frameworks to the specifics. Not generic advice with a name
     attached
   - State their recommendation with the conviction they would actually have
   - Write in their voice per the dossier's voice notes, without fabricated
     quotes
4. **The disagreement map**, the most valuable section. Identify 2 to 4 genuine
   conflicts, name the underlying trade-off for each ("Sharp vs Godin here is
   really reach vs resonance: which constraint binds this account?"), and say
   what evidence would settle it. On Instagram that evidence is often a
   two-week experiment the user can run, so name the test.
5. **Synthesis**, a chair's summary: the recommendation that fits this
   account's stage, niche and constraints; which advisor's warning to keep as a
   tripwire; and concrete next steps with handoffs to the ig skills.

## Live research pass

When the topic is specific (a niche, a platform change, a feature) or the user
wants sources, go beyond the dossiers:

- Use a deep-research skill if one is installed to find what the seated
  advisors have actually written or said about this topic class.
- Otherwise use web search for `[advisor name] + [topic]`, preferring primary
  sources (their own books, blogs, newsletters, talks) over roundups.
- Fold findings into the takes with citations. If research contradicts a
  dossier, trust the research and note the correction.

## Grounding rules (non-negotiable)

- **Label the session as simulation** once, at the top.
- **No fabricated quotes.** Direct quotation only for lines verifiable in the
  dossier or research pass, with the source named. Otherwise paraphrase.
- **No invented endorsements or condemnations.** An advisor can be simulated
  *applying their framework* to the user's account. Never state or imply the
  real person has an opinion about the user's specific account or company.
- **Living advisors get extra care.** Godin, Brunson, Hormozi, Dunford,
  Sutherland, Sharp, Handley and Vaynerchuk are alive and active. Their
  positions evolve. Prefer the research pass for anything time-sensitive, and
  never simulate them commenting on named competitors or controversies.
- **Disagree in substance, not caricature.** Each take is the strongest
  version of the view applied to this case.
- **If the dossier and the question do not overlap** (asking Hopkins about
  Reels), say so in the take and reason by explicit analogy: "Hopkins never saw
  a feed, but his sampling principle maps like this..."

## Output format

```
> Simulated council. Each take is built from the advisor's published
> frameworks and positions, not their actual review.

## The question before the council
[1-2 sentence restatement + what is at stake]

## Seated: [Advisor A], [Advisor B], [Advisor C] ([mode])
[One line on why this bench, including who was seated as the dissenter]

---

### [Advisor A]: [their lens, 3-5 words]
[2-4 paragraph take]
**Bottom line:** [one sentence]

### [Advisor B]: ...

---

## Where the council disagrees
1. **[Conflict]**: [A] says X because [framework]; [B] says Y because
   [framework]. The real trade-off: [underlying tension]. What would settle
   it: [evidence or a two-week test].

## Chair's synthesis
[Recommendation fitted to this account's stage and constraints]
- **Do:** [2-4 concrete next steps]
- **Tripwire:** [which advisor's warning to monitor, and the signal]
- **Execute with:** [skill handoffs]
```

## Adding a custom advisor

Users can extend the bench ("add my own advisor"). Create a dossier from
[references/advisor-template.md](references/advisor-template.md). For
non-famous advisors (a mentor, a top client), the user supplies the positions
and you do not invent them. Save to `~/.claude/instagram/advisors/<name>.md`
so it persists across plugin updates.

## Anti-patterns

- **The agreeing council.** Five takes that bless the existing plan. Re-seat
  with a real dissenter.
- **Name-flavored generic advice.** A take that survives with the name swapped
  is not a take.
- **Quote soup.** Stitching famous one-liners instead of applying the method.
- **Council for execution.** The council decides direction. It does not write
  the caption. Hand off.
- **Twelve advisors on a hook.** Match the bench to the stakes.

## Related skills

- `/ig-brand`: when Dunford's take wins, run the positioning work
- `/ig-growth-plan`: when the direction needs to become a plan
- `/ig-reel`, `/ig-caption`, `/ig-carousel`, `/ig-story`: execute a direction
- `/ig-ads`, `/ig-ad-creative`: when the debate was media or creative strategy
- `/ig-psychology`: Sutherland's behavioral mechanics and Sharp's availability work
- `/ig-audit`: the evidence that settles a disagreement
- `/ig-human`: run the final text through it
