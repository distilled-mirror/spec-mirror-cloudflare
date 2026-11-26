---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Token
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Stream](https://developers.cloudflare.com/api/resources/stream)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Token

##### [Create signed URL tokens for videos](https://developers.cloudflare.com/api/resources/stream/subresources/token/methods/create)

POST/accounts/{account\_id}/stream/{identifier}/token

##### ModelsExpand Collapse

<details>

<summary>

TokenCreateResponse object { token }

</summary>

token: optional string

The signed token used with the signed URLs feature.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20stream.token%20%3E%20(model)%20token_create_response%20%3E%20(schema)>)