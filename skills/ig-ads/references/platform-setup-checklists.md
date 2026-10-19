# Instagram Ads Setup Checklists

Setup for running ads on Instagram through Meta. Do the account foundation once,
then use the pre-launch list on every campaign.

## Contents

- Account foundation
- Pixel and tracking
- Domain and aggregated events
- Audience setup
- Catalog (ecommerce)
- Creative assets
- Messaging setup (click-to-DM)
- Partnership ads setup
- Compliance
- Universal pre-launch checklist

## Account foundation

- [ ] Instagram account is a **Professional account** (Creator or Business)
- [ ] Instagram account connected to a Facebook Page
- [ ] Business Manager (Meta Business Suite) created
- [ ] Business verified, if the ad types in use require it
- [ ] Ad account created inside Business Manager
- [ ] Instagram account added to the Business Manager as an asset
- [ ] Payment method added, time zone and currency correct
- [ ] Team access configured with proper roles

## Pixel and tracking

- [ ] Meta Pixel installed on all pages of the destination site
- [ ] Standard events configured: PageView, ViewContent, Lead, Purchase,
      plus AddToCart and InitiateCheckout for ecommerce
- [ ] Conversions API set up (partner integration is fine)
- [ ] Event match quality above 6 on the optimization event
- [ ] Test events verified in Events Manager
- [ ] Tested inside Instagram's in-app browser on a real phone

See `conversion-tracking.md` for code and validation.

## Domain and aggregated events

- [ ] Domain verified in Business Manager
- [ ] Aggregated Event Measurement configured
- [ ] Top 8 events prioritized (Purchase first, Lead second for most)

## Audience setup

- [ ] Instagram engagement audiences created (profile engagers, video viewers
      at 25/50/75/95%, saved or shared, messaged)
- [ ] Website visitor audiences (30, 60, 90, 180 days) and key-page visitors
- [ ] Customer list uploaded
- [ ] Lookalikes built from purchasers (1%, 1 to 3%)
- [ ] Exclusions ready: buyers, employees, lookalike source

## Catalog (ecommerce)

- [ ] Product catalog connected and feed updating
- [ ] Catalog sales campaigns enabled
- [ ] Instagram Shop tagging set up if used
- [ ] Dynamic product ads configured

## Creative assets

- [ ] Reels and Stories: 1080x1920 (9:16), key content inside the safe zone
      (keep text clear of the top and bottom bands the interface covers)
- [ ] Feed: 1080x1350 (4:5) preferred, 1080x1080 (1:1) acceptable
- [ ] Captions burned in or captions track added (most watch muted)
- [ ] Several concepts ready, not one, so the first read is a comparison
- [ ] Ad copy variations written in the user's voice and run through `/ig-human`
- [ ] UTM parameters on every destination URL

## Messaging setup (click-to-DM)

- [ ] Instagram inbox monitored by a person on a schedule
- [ ] Welcome message and quick replies configured
- [ ] Keyword triggers and replies written (see `/ig-dm`)
- [ ] Response-time expectation stated in the ad or welcome message
- [ ] Conversion definition decided: conversation, qualified, booked, purchased

## Partnership ads setup

- [ ] Creator has granted partnership ad permission on their Instagram account
- [ ] Brand has the creator's handle approved for ads
- [ ] Usage window and paid-amplification rights written down
- [ ] Creator's content ran organically first and earned saves, shares and
      watch-through before any spend
- [ ] Paid partnership label applied as the platform and local law require

## Compliance

- [ ] Special Ad Categories declared if housing, credit, employment, or social
      issues, elections or politics apply
- [ ] Landing page complies with Meta policies
- [ ] No prohibited content, no misleading before and after, no personal
      attribute claims
- [ ] Disclosure for paid partnerships and testimonials as local rules require

## Universal pre-launch checklist

- [ ] Conversion tracking tested with a real conversion
- [ ] Destination loads in under 3 seconds and is mobile-friendly
- [ ] UTM parameters working
- [ ] Budget set correctly (daily vs lifetime), start and end dates correct
- [ ] Targeting matches the intended audience
- [ ] Creative approved
- [ ] Reporting view ready, and a date set for the first operating check
