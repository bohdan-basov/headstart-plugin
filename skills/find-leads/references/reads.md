# Reads

Which pages a fetch reads, and which stay shells or blocked. Spend fetches on the rows that read.

| Read | Result |
|---|---|
| A post's `t.co` link | One fetch returns the redirect target, usually the company domain. |
| Ashby's posting API, `https://api.ashbyhq.com/posting-api/job-board/<slug>` | Every role with its publish date and plain-text description, including the reports-to line. The HTML careers page in front of it is an empty shell. |
| Greenhouse, `https://boards-api.greenhouse.io/v1/boards/<token>/jobs`; Lever, `https://api.lever.co/v0/postings/<company>?mode=json` | Expected to read like Ashby's API, unprobed. The slug or token is usually the company name in the careers URL. |
| LinkedIn guest company pages, `linkedin.com/company/<slug>` | Size band and member count. The slug is a guess: one miss is normal. |
| LinkedIn guest profiles, `linkedin.com/in/<slug>` | Inconsistent; try once. |
| Product Hunt product pages | Render and list the makers: a one-maker read for a founder-run company. |
| Company sites, press, TechCrunch, Companies House, GitHub, the YC mirror | Readable. |
| YC company pages and most sites under ten people | JavaScript shells, title only; the data is elsewhere. |
| `x.com` | A fetch gets nothing; `read_x_profile` and `search_x_posts` are the X reads. |
| Crunchbase, PitchBook, Dealroom's team tab, Indeed, LinkedIn jobs, LinkedIn people search, the LinkedIn People tab | Blocked. People at a company on LinkedIn is read from the team page, the job post or the X profile instead. |
