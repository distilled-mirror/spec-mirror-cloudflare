---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Holds
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zones](https://developers.cloudflare.com/api/resources/zones)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Holds

##### [Get Zone Hold](https://developers.cloudflare.com/api/resources/zones/subresources/holds/methods/get)

GET/zones/{zone\_id}/hold

##### [Create Zone Hold](https://developers.cloudflare.com/api/resources/zones/subresources/holds/methods/create)

POST/zones/{zone\_id}/hold

##### [Update Zone Hold](https://developers.cloudflare.com/api/resources/zones/subresources/holds/methods/edit)

PATCH/zones/{zone\_id}/hold

##### [Remove Zone Hold](https://developers.cloudflare.com/api/resources/zones/subresources/holds/methods/delete)

DELETE/zones/{zone\_id}/hold

##### ModelsExpand Collapse

<details>

<summary>

ZoneHold object { hold, hold\_after, include\_subdomains }

</summary>

hold: optional boolean

<a href="#">Link to this property</a>

hold\_after: optional string

<a href="#">Link to this property</a>

include\_subdomains: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.holds%20%3E%20(model)%20zone_hold%20%3E%20(schema)>)