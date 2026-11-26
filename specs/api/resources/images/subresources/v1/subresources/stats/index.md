---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Stats
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Images](https://developers.cloudflare.com/api/resources/images)

[V1](https://developers.cloudflare.com/api/resources/images/subresources/v1)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Stats

##### [Images usage statistics](https://developers.cloudflare.com/api/resources/images/subresources/v1/subresources/stats/methods/get)

GET/accounts/{account\_id}/images/v1/stats

##### ModelsExpand Collapse

<details>

<summary>

Stat object { count }

</summary>

<details>

<summary>

count: optional object { allowed, current }

</summary>

allowed: optional number

Cloudflare Images allowed usage.

<a href="#">Link to this property</a>

current: optional number

Cloudflare Images current usage.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20images.v1.stats%20%3E%20(model)%20stat%20%3E%20(schema)>)