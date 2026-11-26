---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: To Markdown
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI](https://developers.cloudflare.com/api/resources/ai)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# To Markdown

##### [Convert uploaded files to Markdown](https://developers.cloudflare.com/api/resources/ai/subresources/to_markdown/methods/transform)

POST/accounts/{account\_id}/ai/tomarkdown

##### [List supported Markdown conversion formats](https://developers.cloudflare.com/api/resources/ai/subresources/to_markdown/methods/supported)

GET/accounts/{account\_id}/ai/tomarkdown/supported

##### ModelsExpand Collapse

<details>

<summary>

ToMarkdownTransformResponse object { data, format, mimeType, 2 more }

</summary>

data: string

<a href="#">Link to this property</a>

format: string

<a href="#">Link to this property</a>

mimeType: string

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

tokens: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai.to_markdown%20%3E%20(model)%20to_markdown_transform_response%20%3E%20(schema)>)

<details>

<summary>

ToMarkdownSupportedResponse object { extension, mimeType }

</summary>

extension: string

<a href="#">Link to this property</a>

mimeType: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai.to_markdown%20%3E%20(model)%20to_markdown_supported_response%20%3E%20(schema)>)