---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Context
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Security Center](https://developers.cloudflare.com/api/resources/security_center)

[Insights](https://developers.cloudflare.com/api/resources/security_center/subresources/insights)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Context

##### [Retrieves Security Center Insight Context](https://developers.cloudflare.com/api/resources/security_center/subresources/insights/subresources/context/methods/get)

GET/accounts/{account\_id}/security-center/insights/{issue\_id}/context

##### ModelsExpand Collapse

ContextGetResponse = map\[unknown]

[Link to this property](#)%20security_center.insights.context%20%3E%20(model)%20context_get_response%20%3E%20(schema)>)