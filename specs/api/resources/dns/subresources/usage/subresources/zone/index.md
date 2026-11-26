---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Zone
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[DNS](https://developers.cloudflare.com/api/resources/dns)

[Usage](https://developers.cloudflare.com/api/resources/dns/subresources/usage)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Zone

##### [Get DNS Record Usage](https://developers.cloudflare.com/api/resources/dns/subresources/usage/subresources/zone/methods/get)

GET/zones/{zone\_id}/dns\_records/usage

##### ModelsExpand Collapse

<details>

<summary>

ZoneGetResponse object { record\_quota, record\_usage }

</summary>

record\_quota: number

Maximum number of DNS records allowed for the zone. Null if using account-level quota.

minimum0

<a href="#">Link to this property</a>

record\_usage: number

Current number of DNS records in the zone.

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.usage.zone%20%3E%20(model)%20zone_get_response%20%3E%20(schema)>)