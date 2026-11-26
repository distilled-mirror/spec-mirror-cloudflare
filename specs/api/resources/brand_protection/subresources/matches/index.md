---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Matches
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Matches

##### [Read matches for string queries by ID](https://developers.cloudflare.com/api/resources/brand_protection/subresources/matches/methods/get)

GET/accounts/{account\_id}/brand-protection/matches

##### [Download matches for string queries by ID](https://developers.cloudflare.com/api/resources/brand_protection/subresources/matches/methods/download)

GET/accounts/{account\_id}/brand-protection/matches/download

##### ModelsExpand Collapse

<details>

<summary>

MatchGetResponse object { matches, total }

</summary>

matches: optional array of map\[unknown]

<a href="#">Link to this property</a>

total: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.matches%20%3E%20(model)%20match_get_response%20%3E%20(schema)>)

<details>

<summary>

MatchDownloadResponse object { matches, total }

</summary>

matches: optional array of map\[unknown]

<a href="#">Link to this property</a>

total: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.matches%20%3E%20(model)%20match_download_response%20%3E%20(schema)>)