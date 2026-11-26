---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Content Findings
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Analytics Query](https://developers.cloudflare.com/api/resources/analytics_query)

[Data Security](https://developers.cloudflare.com/api/resources/analytics_query/subresources/data_security)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Content Findings

##### [Top integrations by content findings](https://developers.cloudflare.com/api/resources/analytics_query/subresources/data_security/subresources/content_findings/methods/top_n)

POST/accounts/{account\_id}/analytics/query/data-security/content-findings/top-n

##### ModelsExpand Collapse

ContentFindingTopNResponse = map\[unknown]

Maps field names to values. Keys represent stat names and group-by column names. Values depend on the dataset (strings, numbers, booleans).

[Link to this property](#)%20analytics_query.data_security.content_findings%20%3E%20(model)%20content_finding_top_n_response%20%3E%20(schema)>)