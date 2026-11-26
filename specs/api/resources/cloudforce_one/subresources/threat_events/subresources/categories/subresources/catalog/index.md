---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Catalog
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Events](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events)

[Categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/categories)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Catalog

##### [List all event categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/categories/subresources/catalog/methods/list)

GET/accounts/{account\_id}/cloudforce-one/events/categories/catalog

##### ModelsExpand Collapse

<details>

<summary>

CatalogListResponse = array of object { killChain, name, uuid, 3 more }

</summary>

killChain: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

uuid: string

<a href="#">Link to this property</a>

mitreAttack: optional array of string

<a href="#">Link to this property</a>

mitreCapec: optional array of string

<a href="#">Link to this property</a>

shortname: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.categories.catalog%20%3E%20(model)%20catalog_list_response%20%3E%20(schema)>)