# Fit

Give each company a verdict against the brief: **in** when none of the six rules fires, **out**
with the rule named. Fit is judged after the signal and before anyone is named: a large company
raising a round is a signal, and for a brief that buys for tiny teams it is out at rule 3. Field
5 holds the customer's values for each rule.

## The six rules

1. **Poster is not the company**, and no real company resolved behind it.
2. **Cannot pay**: below the brief's stage or size floor, or no money evidence.
3. **Past the ceiling**: beyond the brief's size or stage ceiling. For a brief that sells to
   founders who still build: engineering hires on the team page, or a product past its first
   release (a funded two-person company whose app shipped a year ago is out). A brief with no
   ceiling says `none`.
4. **Wrong vertical, geography or stack.**
5. **The signal is not growth**: a backfill, a single role, a round outside its window, a funded
   company outside field 3's shape.
6. **On the suppression list**, field 7.

## Reading size and stage

Read size twice: the LinkedIn guest company page's band and member count
(`linkedin.com/company/<slug>`; the slug is a guess, budget one wasted fetch), and the open-role
count on the company's ATS board or the team page. The band is typed by an admin and can be off
by two times; the roles and the team page are what the company shows today. Stage comes from the
funding signal itself or the press behind it, with a 30 to 90 day recency.

A company under ten people often has no second read: no team page, no board, an unknown LinkedIn
slug. Take the one read and mark the size line `inferred`; the company stays in the run.

## The verdict line

    <Company> (<domain>): in. Rules 1–6 checked. Size: <band> (<URL>), <role count> (<URL>). Stage: <stage> (<URL>).
    <Company> (<domain>): out, rule 3. <what was read> (<URL>).
