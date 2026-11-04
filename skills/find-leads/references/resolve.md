# Resolve

Turn each signal into a company keyed by its domain, or drop it with a reason. The domain is the
key every later read hangs on.

## From a post to a domain

- The link in the post: `search_x_posts` returns it already expanded, usually the company domain.
- The poster's bio, pinned post or profile website line (`read_x_profile` returns them).
- A `jobs@` or `careers@` address in the post.
- The Product Hunt page, a press article, a directory entry: each names the domain.
- Web search on the company name, when the post gives only the name.

A signal whose company none of these keys to a domain is dropped: `no domain`. The other drop
reasons: `agency, no employer` (below) and `duplicate of <domain>`.

## The poster is a route to the company

About half of job posts come from agencies, marketplaces and boards; a funding post may be a
journalist's, an investor's or an employee's. The company behind the signal is the one that
hires or raised; the poster is a route to it. On every hiring signal the **agency test** runs
first:

1. The poster's own company card and industry: an employee or founder of the hiring company
   passes; a recruiter, agency or job board fails.
2. Posting rate against headcount: a handle posting dozens of roles a week for a ten-person
   company is a board or an agency.
3. The company's own careers board carries the role (`reads.md` gives the board URLs that read).

Pass: resolve to the hiring company. Fail with the employer named in the post: resolve to the
employer, note the poster as the route. Fail with no employer named: drop, `agency, no employer`.
