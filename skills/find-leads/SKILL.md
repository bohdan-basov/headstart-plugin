---
name: find-leads
description: "Leads for what you sell: decision makers at companies that show a buying signal and fit your brief, with why now. Use when the user asks for leads, clients, or who to reach out to."
---

# Find leads

Two tools from the `headstart` connector, `search_x_posts` and `read_x_profile`, plus your own
web search and fetch. A **lead** is a decision maker at a company that shows a signal and fits
the brief; the person may never have posted, and the signal may be someone else's post. One
**run** returns ten leads unless the user names a count. Three to five companies examined per
lead is normal.

Six steps, in order. Read the step's file before the step; each step ends on a done-when you
tick in the transcript before the next starts. `references/signals.md` is the catalog of signal
types and `references/reads.md` the pages that read and the pages that do not: open them when
Brief, Sweep or Resolve calls for them.

## 1. Brief: read `references/brief.md`

Receive the brief, or draft it from the user's own site and ask one round for the rest. On
claude.ai the brief lives in the Project instructions between chats: read it there before asking,
and end the run by returning it extended for the user to paste back. **Done when** fields 2, 3 and
4 are answered and the other five are answered or `none`.

## 2. Sweep: read `references/sweep.md`

Read field 8 first: a parked company skips to Name. Collect signals of the types field 4 names,
from the sources the catalog gives each type. **Done when** every signal carries its type, its
date, its URL and the raw poster.

## 3. Resolve: read `references/resolve.md`

Turn each signal into a company keyed by its domain, or drop it with a reason. On a hiring signal
the agency test runs first. **Done when** no signal lacks a domain or a drop reason.

## 4. Fit: read `references/fit.md`

Give each company a verdict by the six rules with the brief's field 5 values: in when none fires,
out with the rule named. **Done when** every company carries a verdict, the rule that fired if
out, and the URLs behind it.

**Loop.** When Fit leaves fewer companies in than the run asks for, return to Sweep with new
angles or another signal type from field 4; companies already resolved stay resolved.

## 5. Name: read `references/name.md`

Find the person field 2's role rule names, from public pages, and confirm the role and a public
URL. **Done when** a person with a public URL is named, or the company goes to field 8 as
`fits, person not found`.

## 6. Why: read `references/why.md`

Write each lead as the block below. **Done when** every lead is a complete block and every fact
in it carries a URL or the word `inferred`.

## The lead block

    1. Name, Role at Company (domain)
       Person: public URL (X profile, LinkedIn, or the company site).
       Company: size as read, stage.
       Signal: type, date, URL.
       Fit: one line; the six rules checked, none fired.
       Why now: one or two sentences, from what the job text or the press release says the
       company is trying to do.
       Opener context: the fact the customer leads with.
       Warm path: the shared investor, batch, employer or community, or none.
       Evidence: a URL per claim above, or `inferred`.

## The report

Open with one line: how many leads, and the signal types the sweep covered. Then the numbered
blocks. Then the brief, whole, with every company shown added to field 7 and every
`fits, person not found` added to field 8. Close with the spend line:

    Spend: N searches, N profile reads, N web fetches; N companies examined for N leads.

When fewer than the count clear Fit and Name after the loop, say how many did and which signal
types the sweep did not reach. The list holds leads only; the gap is said, never filled.
