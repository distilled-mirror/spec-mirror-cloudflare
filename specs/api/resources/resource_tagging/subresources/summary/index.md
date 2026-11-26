---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Summary
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Resource Tagging](https://developers.cloudflare.com/api/resources/resource_tagging)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Summary

##### [List tag key summary](https://developers.cloudflare.com/api/resources/resource_tagging/subresources/summary/methods/get)

GET/accounts/{account\_id}/tags/summary

##### ModelsExpand Collapse

<details>

<summary>

SummaryGetResponse = array of object { key, values }

Contains an array of tag keys with their distinct values.

</summary>

key: string

A tag key.

<a href="#">Link to this property</a>

values: array of string

All distinct values for this tag key.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20resource_tagging.summary%20%3E%20(model)%20summary_get_response%20%3E%20(schema)>)