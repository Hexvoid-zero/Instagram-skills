# Brand Voice

Voice is how the account sounds everywhere. Tone is how much of that voice you
turn up or down for a given moment. A reply to an angry comment and a launch
Reel use the same voice at very different tones.

`brand.md` keeps a short voice summary that every skill reads. The full profile
lives in `~/.claude/instagram/voice.md`. This reference covers how to build
it, how tone changes by context, and how other skills apply it.

## Build the profile from evidence

Three adjectives picked in a meeting ("friendly, bold, expert") do not
constrain anything, because every brand claims them. Build the profile from
writing and speech that already exist and already work.

**Sources, strongest first:**

1. **Posts that performed.** The Reels and captions that beat the median in
   `log.md`. Pick by the numbers, not by what the team likes.
2. **The person's own spoken and written voice.** Voice notes, DMs they wrote
   themselves, transcripts of Reels they filmed. Early accounts usually sound
   like the founder or creator, whether or not anyone decided that.
3. **Sales and support conversations.** How they explain the offer in a DM is
   often clearer than the bio.
4. **Customer comments and reviews.** These give vocabulary more than voice:
   the words buyers use for the problem and for you. They feed **Customer
   Language** in `brand.md`.
5. **Copy you would never write.** A competitor caption or a draft that felt
   wrong. Saying why it is wrong defines the edges faster than describing the
   middle.

**Steps:**

1. Collect 10 to 20 samples, each labeled with format and, where you have it,
   how it performed. For Reels, use transcripts.
2. Note observable traits: sentence length, first person, contractions, jargon,
   numbers vs stories, humor and where, slang, how bad news is handled, how
   they open and close.
3. Write 3 to 5 voice attributes. Each needs a **means**, a **doesn't mean** and
   a real line from the samples. The "doesn't mean" column does the work: a
   "direct" that does not rule out curt, or a "playful" that does not rule out
   jokes in a complaint reply, will not change a draft.
4. Test it. Put an unlabeled draft written to the profile next to a competitor's
   caption and ask someone who knows the account which is theirs. If they cannot
   tell, the attributes are too generic.
5. Confirm with the user. Voice is a choice the account makes.

**Example profile** (a fictional strength coach for new mothers):

| Attribute | Means | Doesn't mean | Line from the samples |
|---|---|---|---|
| Plain-spoken | Short words, numbers over adjectives, time stated in minutes | Dumbed down or vague | "Twenty minutes. No equipment. Baby can watch." |
| On her side | Takes the mother's view against guilt and gym culture | Snarky about other coaches by name | "You are not behind. Nobody gave you a map." |
| Calm about bodies | States what changes and what helps without drama | Cold or clinical | "Your core feels different. Here is what is normal and when to ask a physio." |
| Dry humor, rarely | One light line where the stakes are low | Jokes about pain, mood or medical issues | "Yes, you can do squats holding a toddler." |

## Tone by context

Hold the attributes constant and change the intensity.

| Context | Turn up | Turn down | Rule of thumb |
|---|---|---|---|
| **Reels** | Personality, opinion, specifics | Hedging, filler | The first two seconds carry the voice. Say it the way you would to a friend. |
| **Captions** | Detail, proof, the next step | Repeating the Reel | Add what the video could not. Front-load the hook. |
| **Stories** | Casual, immediate, behind the scenes | Polish | The loosest the voice gets, still inside the attributes. |
| **DMs** | One person at a time, short, a single ask | Pitch, hype | Write like a person messaging a person. |
| **Comment replies** | Warmth, specific answers | Marketing claims | Answer first. Move complicated threads to DM. |
| **Ads** | Specifics, proof, a plain ask | Superlatives | If the ad would read the same with a competitor's name, it is too generic. |
| **Complaints and crisis** | Calm, plain facts, ownership | Humor, defensiveness | Precision over personality. See `/ig-pr`. |

## Before and after

**Launch caption**
- Before: "We're excited to announce our powerful new program, designed to help you transform your fitness journey."
- After: "Twelve weeks. Twenty minutes a day. Doors open Monday for 30 mothers."

**Comment reply**
- Before: "Thanks so much for your comment! We appreciate your support."
- After: "Short answer: yes, from week 6 if your doctor cleared you. Sending the checklist."

**DM opener**
- Before: "I hope this message finds you well. I wanted to reach out about our innovative offering."
- After: "Saw your Story about the 5am workouts. If sleep is the problem, I have a 20 minute plan that fits nap time."

## Words

The brand word list holds terms specific to this account:

| List | What goes in it | Example |
|---|---|---|
| **Terms we own** | What the account calls things, used the same way everywhere | "Members," never "clients" |
| **Customer words** | The audience's phrases for the problem | "Mum guilt", "pelvic floor fear" |
| **Never use** | Words that break the voice, with the reason | "Journey" (every program says it); "bounce back" (our audience is tired of it) |
| **Category words to avoid** | Terms every competitor uses | "Transform your body" |

Keep the reason beside each "never use" word. For generic AI-sounding words,
`/ig-human` already carries the slop list.

## Personal voice and client voices

When writing as a specific person (a founder, a creator, a client), read that
person's profile before the brand summary. Capture:

- How they open and close
- Sentence habits (length, fragments, questions, favorite phrases)
- Emoji, punctuation and formatting habits
- Templates for message types they send often
- Things they never say

Refresh it every quarter from their recent posts and fold in the edits they
make to your drafts. Their edits are the most accurate voice data you will get.
Store the account's own voice at `~/.claude/instagram/voice.md`. For an agency
with several clients, keep `~/.claude/instagram/voices/<client>.md`.

## How other skills apply it

- **Drafting skills** (`/ig-reel`, `/ig-caption`, `/ig-carousel`, `/ig-story`,
  `/ig-dm`, `/ig-reply`, `/ig-ad-creative`) read the attributes and the tone row
  for the format before writing. Check the draft against each attribute's
  "doesn't mean" column.
- **`/ig-human`** judges the draft against the profile instead of general
  taste, and flags lines that break an attribute.
- **Review output:** the revised copy, then one line per change naming the
  attribute or tone rule it serves. Skip the line for a typo or fact fix.
- **When top-performing posts keep breaking the profile** in the same way, the
  profile is probably wrong. Raise it with the user, log it in Learnings and
  update the profile if they agree.

---

*Tone-by-context, word lists and per-person voice guides adapted from Wispr
Flow's brand-voice skill, published under MIT in
[skills-marketing-library](https://github.com/retieedra-profound/skills-marketing-library).
Rewritten for Instagram.*
