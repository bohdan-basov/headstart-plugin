# Sweep

Collect signals from the sources field 4's types name; `signals.md` gives each type its event,
its window and where it is read. A signal is a public event with a date and a URL; the poster
is whoever posted it, recorded as is.

## Parked first

Field 8 before the first search: every parked company goes straight to Name with its stored
domain and signal URL, and counts toward the run.

## X search is the sweep

X search over founders' and companies' own words finds the hiring, funding and about-to-raise
signals; one well-shaped query returned every signal that became a lead in the walkthroughs
behind this skill. Shape a query as an OR group of the phrases a founder or an employee writes
on the day, with `since:` set to the window's start, `-filter:retweets`, `lang:en`, latest
first:

- funding: `("raised our pre-seed" OR "closed our pre-seed" OR "announcing our seed") since:<date> -filter:retweets lang:en`
- hiring: `"we're hiring" ("founding engineer" OR "backend engineer" OR engineers) (seed OR "series a") since:<date> -filter:retweets lang:en`
- about to raise: `"solo founder" ("pre-seed" OR "seed round") since:<date>`
- stated ask: the service in the buyer's words, `("looking for a" OR "anyone recommend") <service> since:<date>`
- launch: `("we just launched" OR "launching today") since:<date>`

Read the whole page before the next query; the next query answers what the last page showed. A
page under five on-topic posts earns a changed shape: a wider OR group, another phrase, another
type. A full page that was almost all on topic earns page two.

## The web resolves and confirms

Web search for "funded and hiring this month" returns guides and aggregators; use it after a
company name is in hand, to confirm a round or find the board. Fetch the sources a type names
directly: press releases, ATS boards, Product Hunt, batch and accelerator directories, Companies
House, the YC mirror. Field 6's warm paths are lists to read whole: an investor's portfolio page,
a batch page, a community's member directory.

## What each signal carries

Type, date, URL, raw poster (handle or outlet), and the words that make it a signal: the role
titles and count for hiring, the amount and what the money is for when stated for funding, the
proxy for about to raise. Keep every in-window signal, including the ones whose company is still
unknown; Resolve sorts them.
