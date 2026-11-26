---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Colos
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[DEX](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dex)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Colos

##### [List Cloudflare colos](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dex/subresources/colos/methods/list)

GET/accounts/{account\_id}/dex/colos

##### ModelsExpand Collapse

<details>

<summary>

ColoListResponse object { airportCode, city, countryCode }

</summary>

airportCode: string

Airport code

<a href="#">Link to this property</a>

city: string

City

<a href="#">Link to this property</a>

countryCode: string

Country code

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dex.colos%20%3E%20(model)%20colo_list_response%20%3E%20(schema)>)