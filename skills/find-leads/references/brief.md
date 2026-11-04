# Brief

The customer's description of who buys from them, in eight fields. A field is answered or marked
`none`. The run starts once fields 2, 3 and 4 are answered.

1. **Sells**: what the customer sells, one line.
2. **Buys**: the decision maker as roles, never names. A hiring platform: the talent owner or the
   leader the open roles report to. A retainer for senior engineers: the founder or a technical
   co-founder / CTO who still builds.
3. **Company shape**: size band, stage, vertical, geography, stack.
4. **Signals**: the types from `signals.md` that say "now" for this customer, each with a
   freshness window; the catalog's default window unless the customer tightens it.
5. **Exclusions**: the customer's values for the six fit rules in `fit.md`.
6. **Warm paths**: investors, batch, accelerator, former employers, communities the customer
   shares with buyers.
7. **Suppression**: existing customers, people already contacted, and every company a previous
   run showed. A company here stays out of every later run.
8. **Parked**: companies that fit but where no person was found: company, domain, signal URL, the
   step it stopped at. Read before Sweep, retried at Name only.

## How a brief is made

When the user pastes a brief or the Project instructions hold one, take it as written and go on.
Otherwise fetch the customer's own site first and draft fields 1 to 3 from it; ask only for what
the site could not tell you, in field order, in one round; fill fields 4 and 5 with the catalog's
defaults and the shape's own exclusions when the user leaves them to you. Show the finished brief
as the markdown block below, so the user owns it and pastes it into later chats.

## The block

    ## Brief
    1. Sells:
    2. Buys:
    3. Company shape:
    4. Signals:
    5. Exclusions:
    6. Warm paths:
    7. Suppression:
    8. Parked:

## Example

    ## Brief
    1. Sells: senior product engineers on a monthly retainer, MVP to first release.
    2. Buys: the founder, or a technical co-founder / CTO who still builds.
    3. Company shape: 1–8 people, pre-seed to seed, software, hours overlapping US/EU.
    4. Signals: funding (90 days, with what the money is for); about to raise (60 days);
       stated ask (30 days).
    5. Exclusions: engineering hires on the team or a product past first release; no money
       and no raise in sight; non-software; an agency or studio itself.
    6. Warm paths: none
    7. Suppression: none
    8. Parked: none
