# Loop Guardrails and Compliance

Loops act on a schedule, sometimes with money or a public voice, and on people's
messages. These rules keep a loop from doing harm. Apply them to every loop that
posts, replies, messages, spends or touches personal data.

## The two-tier action model

**Tier 1, autonomous-safe** (a loop may do these unattended): read data,
analyze, diff, score, **draft** and **stage** work for review.

**Tier 2, gated** (human checkpoint by default): **post or schedule** content,
**reply** to a comment, **send** a DM, **spend** or shift budget, **delete or
hide** comments, **change** profile or ad account settings, **contact** a
creator or journalist.

A Tier-2 action may run without a per-action check only if the user has
explicitly authorized it and it is bounded by caps and an allowlist. Absent
that, the loop stages a draft and a human approves.

## Instagram-specific rules

- **No automated engagement.** Do not run loops that like, follow, unfollow,
  comment or DM at scale through unofficial tools. It violates Instagram's
  terms, risks the account, and reads as spam. Loops draft. A human posts, or
  Meta's own scheduling and automation features do it.
- **Messaging windows and consent.** Respond within the platform's messaging
  rules. Do not message people who have not contacted you or opted in through a
  keyword trigger. Honor "stop" immediately and keep a suppression list.
- **Comment replies stay human.** Replies are staged. Critics, complaints and
  sensitive topics always escalate.
- **Scraping.** Use official exports, the user's own insights, or a data
  provider whose terms allow it. Do not log into accounts or bypass access
  limits. When a source fails, report it as stale.

## Spend guardrails (ad loops)

- **Hard caps.** A daily and weekly ceiling the loop can never exceed. Halt and
  alert when approached.
- **Per-run change limit.** Cap budget movement per run (for example 20% or
  less) so a bad read cannot reallocate everything.
- **Allowlist.** Only named campaigns are eligible for autonomous changes.
- **Judge on revenue.** Do not optimize CTR or CPA into a revenue loss.

## Publish and send guardrails

- **Staging queue plus approval** for anything public or outbound.
- **Volume caps** per run and per recipient.
- **Suppression first.** Check the do-not-contact list before every send.
- **Creator outreach** is staged. Contracts and rights terms go to a human.

## Compliance

- **FTC and local ad rules.** Disclose paid partnerships and material
  connections with the platform's label and clear wording. Use testimonials only
  with permission. No fabricated or misleading claims.
- **Giveaways and contests.** Follow Instagram's promotion guidelines and local
  law. State that the promotion is not sponsored by Instagram.
- **GDPR, CCPA and similar.** Process personal data on a lawful basis, honor
  deletion and opt-out requests, minimize what is stored.
- **Meta ad policies.** Special Ad Categories, prohibited content and personal
  attribute rules apply to any ad loop.
- **Email and SMS** (if a loop hands off to them): CAN-SPAM, CASL and consent
  rules.

When a loop cannot confirm consent, permission or terms compatibility, its stop
condition is **do not act**. Stage it for a human.

## PII handling

- No raw handles, messages or names in state files or run logs where an ID will
  do. Use thread or comment IDs.
- Pull the minimum personal data needed to decide.
- Keep exports and drafts out of shared locations unless intended.

## Always-escalate list

Never runs fully autonomously, regardless of authorization:

- Negative or crisis mentions, call-outs, complaints, and legal, medical or
  financial-sensitive topics.
- Newsjacking and trend-jacking around tragedies, politics or disasters.
- Large creators, press, and strategic partners.
- Anomalies in spend or revenue. Flag, do not self-correct.
- Anything that deletes data or reaches a large audience at once.
- Messages from minors or about self-harm. Do not run engagement drafts on
  these. Escalate to the account owner.

## Kill switch

Every scheduled loop needs a manual off switch, and you should know how to stop
all loops fast (disable the schedules, or a global flag the loop bodies check).
Document it where the loops are scheduled.

## Pre-launch checklist

- [ ] Every action is classified Tier 1 or Tier 2.
- [ ] Tier-2 actions are staged, or bounded by explicit authorization, caps and an allowlist.
- [ ] Spend loops have a hard cap and a per-run change limit.
- [ ] Send loops check suppression and have volume caps.
- [ ] No automated engagement outside Meta's own tools.
- [ ] Disclosure and promotion rules are satisfied, with "do not act" as fallback.
- [ ] No raw PII in state or logs.
- [ ] Always-escalate cases route to a human.
- [ ] There is a documented kill switch.
