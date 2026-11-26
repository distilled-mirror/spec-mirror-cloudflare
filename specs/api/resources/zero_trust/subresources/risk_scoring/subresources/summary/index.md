---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Summary
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Risk Scoring](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Summary

##### [Get risk score info for all users in the account](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring/subresources/summary/methods/get)

GET/accounts/{account\_id}/zt\_risk\_scoring/summary

##### ModelsExpand Collapse

<details>

<summary>

SummaryGetResponse object { users }

Risk summary of the users in an account.

</summary>

<details>

<summary>

users: array of object { email, event\_count, last\_event, 3 more }

Users on this page, with their risk summary.

</summary>

email: string

Email address of the user.

<a href="#">Link to this property</a>

event\_count: number

Number of risk events of the user.

minimum0

<a href="#">Link to this property</a>

last\_event: string

Time of the most recent risk event of the user.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

max\_risk\_level: "unset" or "info" or "low" or 2 more

Highest risk level. The value is unset when no event maps to a configured behavior.

</summary>

One of the following:

"unset"

<a href="#">Link to this property</a>

"info"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Name of the user.

<a href="#">Link to this property</a>

user\_id: string

User ID (UUID v4).

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(model)%20summary_get_response%20%3E%20(schema)>)