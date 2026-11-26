---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Content
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Logpush](https://developers.cloudflare.com/api/resources/logpush)

[Transformers](https://developers.cloudflare.com/api/resources/logpush/subresources/transformers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Content

##### [Get transformer content](https://developers.cloudflare.com/api/resources/logpush/subresources/transformers/subresources/content/methods/get)

GET/accounts/{account\_id}/logpush/transformers/{transformer\_id}/content

##### ModelsExpand Collapse

<details>

<summary>

ContentGetResponse object { content }

</summary>

content: optional string

The SQL query content.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20logpush.transformers.content%20%3E%20(model)%20content_get_response%20%3E%20(schema)>)