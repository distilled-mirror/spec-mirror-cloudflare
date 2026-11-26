---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Regions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Load Balancers](https://developers.cloudflare.com/api/resources/load_balancers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Regions

##### [List Regions](https://developers.cloudflare.com/api/resources/load_balancers/subresources/regions/methods/list)

GET/accounts/{account\_id}/load\_balancers/regions

##### [Get Region](https://developers.cloudflare.com/api/resources/load_balancers/subresources/regions/methods/get)

GET/accounts/{account\_id}/load\_balancers/regions/{region\_id}

##### ModelsExpand Collapse

RegionListResponse = unknown

[Link to this property](#)%20load_balancers.regions%20%3E%20(model)%20region_list_response%20%3E%20(schema)>)

RegionGetResponse = unknown

A list of countries and subdivisions mapped to a region.

[Link to this property](#)%20load_balancers.regions%20%3E%20(model)%20region_get_response%20%3E%20(schema)>)