---
title: Search
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Search

##### [Search Threat Signals articles using AI Search](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/search/methods/search)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/search

##### ModelsExpand Collapse

<details>

<summary>

SearchSearchResponse object {count, results }

</summary>

count: number

Number of unique article candidates returned in this response. Equal to results.length.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

results: array of object {article\_id, dataset\_id, event\_id, 3 more }

</summary>

article\_id: string

formatuuid

<a href="#">Link to this property</a>

dataset\_id: string

formatuuid

<a href="#">Link to this property</a>

event\_id: string

formatuuid

<a href="#">Link to this property</a>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

score: number

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.search%20%3E%20(model)%20search_search_response%20%3E%20(schema)>)