---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Previews
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Load Balancers](https://developers.cloudflare.com/api/resources/load_balancers)

[Monitors](https://developers.cloudflare.com/api/resources/load_balancers/subresources/monitors)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Previews

##### [Preview Monitor](https://developers.cloudflare.com/api/resources/load_balancers/subresources/monitors/subresources/previews/methods/create)

POST/accounts/{account\_id}/load\_balancers/monitors/{monitor\_id}/preview

##### ModelsExpand Collapse

<details>

<summary>

PreviewCreateResponse object { pools, preview\_id }

</summary>

pools: optional map\[string]

Monitored pool IDs mapped to their respective names.

<a href="#">Link to this property</a>

preview\_id: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20load_balancers.monitors.previews%20%3E%20(model)%20preview_create_response%20%3E%20(schema)>)