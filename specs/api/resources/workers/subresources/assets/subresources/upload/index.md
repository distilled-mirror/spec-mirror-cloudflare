---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Upload
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Assets](https://developers.cloudflare.com/api/resources/workers/subresources/assets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Upload

##### [Upload Worker Assets](https://developers.cloudflare.com/api/resources/workers/subresources/assets/subresources/upload/methods/create)

POST/accounts/{account\_id}/workers/assets/upload

##### ModelsExpand Collapse

<details>

<summary>

UploadCreateResponse object { jwt }

</summary>

jwt: optional string

A “completion” JWT which can be redeemed when creating a Worker version.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.assets.upload%20%3E%20(model)%20upload_create_response%20%3E%20(schema)>)