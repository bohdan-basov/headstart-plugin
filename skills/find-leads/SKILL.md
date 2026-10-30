---
name: find-leads
description: "Leads on X: people whose posts show they need what the user sells. Use when the user asks for leads or clients, or for people who need their service right now."
---

# Find leads

Two tools from the `headstart` connector: `search_x_posts` and `read_x_profile`.

## Steps

Work in this order. Each step ends on a check you can tick before the next starts.

### 1. Read the brief

Take three things from the user's message: the **service** they sell, the **buyer** who pays
for it (a role or a kind of business), and the **count** (ten unless they say otherwise). Take
place, language and budget floor when stated. When the service or the buyer is missing, ask one
question that covers both and end the turn. Otherwise state your reading in one line and go on.

Done when: service, buyer and count are written down.

### 2. Plan the angles

Before the first search, list the angles a buyer of this service posts from:

- asking for it ("looking for a web designer", "need a website for my")
- asking for a recommendation ("anyone recommend a web designer")
- hiring for it ("hiring a web developer")
- complaining about their own ("my website is embarrassing", "still don't have a website")
- complaining about a provider ("our agency ghosted us", "paid for a site and it's unusable")
- stalled doing it themselves ("been rebuilding our site for months")
- sourcing it for a client ("client needs a site, who do you recommend")

An eighth, pricing ("how much should a website cost"), when the others run thin.

A **trigger** post announces a change (a new role, money arrived, a launch or rebrand, moving
platforms) without naming the gap: a reason to look, not a need. It goes on a **watch** list in
step 3.

Turn each angle into one query: an OR group of three to six phrases in the buyer's own words. An
OR group fills a page; a single exact phrase returns one or two posts for the same call. Leave
`since` and `until` out on the first pass: results come newest first and you cut by date when you
judge. Search replies too: a need often sits in one.

Done when: the queries are written, one per angle.

### 3. Search, one call at a time

Run one query, read the page, then write the next: each query answers what the last page showed.
One angle per call.

After a thin page (under five on-topic posts), change the shape: widen the OR group, drop a
filter, switch angle. A page that was full and almost all on topic earns a second page with
`next_cursor`; otherwise a new angle beats page two. Both count as searches.

On every page, check each post with what is already there, the text and the author header (bio,
followers, location, DMs open):

1. The post shows one of the angles' needs, in the poster's own words.
2. The need is still open.
3. The post is under a month old.
4. The header reads as a buyer: a business or a paying role in the bio. A developer, designer
   or agency asking for the same service is a seller.

A post that passes all four goes on the **shortlist** with six fields: handle, the post's words
and date, the post URL, the reply count, and the header facts.

A trigger post, a change announced without the gap named, puts the handle on the **watch**
list. Need angles run first. When the
shortlist is short and budget remains, one `from:` search over the watch handles OR-ed together,
with the service words and no date window, looks for the gap in their other posts. A watch
handle whose other post names the gap moves to the shortlist with that post as its post (its URL
in the header) and the change as a reason it is warm; one whose posts stay silent is dropped.

The same `from:` search, over several shortlisted handles, shows what else an ambiguous candidate
said. It counts as a search.

Done when: the shortlist holds about fifteen and every watch handle has a need post or is
dropped, or the twelfth search is done. Twelve is the budget. Short of fifteen with searches
left, run another angle. When the twelfth search is done, go on with what you have.

### 4. Read every shortlisted profile

Request the profile reads for the whole shortlist in one go: at most fifteen, cheap and
independent of each other. Every name in the answer has a profile read behind it. From each
profile confirm:

- **A buyer.** Bio, Website line and pinned post show a business or a paying role.
- **A history.** Post count and join date show an account that has been around. A thin or new
  handle stays on the list with the catch stated.
- **Nothing contradicts the need.** The pinned post and bio neither sell the service nor say
  the job is done.

Drop a candidate that fails buyer or contradiction. Keep one that fails only history, with the
catch.

Done when: every shortlisted handle has a read and is marked in or out.

### 5. Judge against the bar

Someone is **worth a look** when their post shows one of the angles' needs in their own words;
the need is still open (no "found someone" from them, no "don't need one yet" in the post); the
post is under a month old, and for an ask the nearer two weeks the better; and their profile
shows a business or a role that holds the budget.

A stated low budget, a crowded reply thread, a post near the month line, or a thin handle (default
avatar, digits for a name, days old) keep a person on the list, lower them, and go in the why as
the **catch**. A poll, a general question about the topic, a finished job, a negated need, or a
seller asking for subcontractors shows no need and stays off the list, hedge or no hedge.

Rank those who clear the bar by **warmth**: how plainly the post states the need and whether it
names a time or a budget, how clearly the profile pays, how recent, how crowded the thread against
the author's following.

Done when: every candidate is in with its catch or out, and the ins are in warmth order.

### 6. Report

Open with one line: how many, the order, and what holds for all of them so it is said once,
the window and whether DMs are open. "Ten, warmest first. All posted in the last two weeks,
all DMs open."

Then one numbered list, warmest first. Each **lead** is this block:

    1. @handle (Oct 27) https://x.com/handle/status/…
       Who they are, from the profile: the business or role, the place, one count when it
       says something. What they said, in the post's own words, with the reply count. Why
       they are worth a look, with the catch.

The header carries the rank, the handle, the post's month and day and the post URL, bare.
The paragraph is three sentences with those three jobs, in that order. The header's one link
and the three sentences are the whole block; the position in the list is the warmth. The why ends
where the
message begins: an angle fits in a clause ("lead with a portfolio", "pitch as a vendor"), and
the customer writes the message. DMs closed goes in the catch.

Example:

    5. @_startuphacker (Oct 19) https://x.com/_startuphacker/status/2112227311139356881
       Founder of Tyce, construction AI, Toronto, 5,400 followers, DMs open. Announced a $2M
       pre-seed and wrote "We're hiring founding engineers in Toronto (full-stack and AI
       agents)", asking people to DM or tag someone, 60 replies. A technical founder who
       already admitted his weak spot is anything that is not building, which is the profile
       that outsources sourcing; the catch is a $2M round, so fees have to fit a small budget.

When more cleared the bar than the count asked for, the rest go under one line, "Also cleared
the bar, lower:", header line only, and only people who cleared the bar.

Close with one line about the list: the angles your queries covered, in the buyer's words, and the
offer
of a next round that names the angle or the window it would use. When fewer cleared the bar
than asked: how many did, how many searches it took, which angles were not reached, and the
same offer. The list holds only people worth a look; the gap is said, never filled.

For a count above ten: one round of ten, report, offer the next round. The budget is per round.

Done when: the opening line, every block with its three sentences, and the closing line are
written.
