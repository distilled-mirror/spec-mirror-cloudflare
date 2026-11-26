---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Type
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Security Center](https://developers.cloudflare.com/api/resources/security_center)

[Insights](https://developers.cloudflare.com/api/resources/security_center/subresources/insights)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Type

##### [Retrieves Security Center Insight Counts by Type](https://developers.cloudflare.com/api/resources/security_center/subresources/insights/subresources/type/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/security-center/insights/type

##### ModelsExpand Collapse

<details>

<summary>

TypeGetResponse = array of object { count, value }

</summary>

count: optional number

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_center.insights.type%20%3E%20(model)%20type_get_response%20%3E%20(schema)>)