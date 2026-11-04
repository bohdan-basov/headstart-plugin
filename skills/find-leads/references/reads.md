# Reads

Which pages a fetch reads from inside the chat host, and which are blocked (probed from claude.ai,
2026-11-05). Spend fetches on the rows that read.

| Read | Result |
|---|---|
| A post's `t.co` link | Blocked, and unneeded: `search_x_posts` returns every link already expanded to its target, usually the company domain. |
| Ashby's posting API, `https://api.ashbyhq.com/posting-api/job-board/<slug>` | Every role with its publish date and plain-text description, including the reports-to line. The HTML careers page in front of it is an empty shell. |
| Greenhouse, `https://boards-api.greenhouse.io/v1/boards/<token>/jobs`; Lever, `https://api.lever.co/v0/postings/<company>?mode=json` | Public JSON boards, read like Ashby's; large, so ask for the first part. The slug or token is usually the company name in the careers URL. |
| LinkedIn, every page (company pages, profiles, jobs, people search) | Blocked. Size comes from the team page, press, a directory (TheOrg, Built In, the YC directory) or the open-role count; a person's role from the team page, the job post, press or the X profile. |
| Product Hunt product pages | Render and list the makers: a one-maker read for a founder-run company. |
| Company sites (including tiny ones), press, press-release wires, TechCrunch, Companies House, GitHub, YC company and jobs pages, TheOrg, Built In, investors' job boards | Readable; the page body follows a block of metadata. |
| `x.com` | A fetch gets nothing; `read_x_profile` and `search_x_posts` are the X reads. |
| Crunchbase, PitchBook, Dealroom's team tab, Indeed | Blocked. Funding facts come from the press and the founder's own post. |
