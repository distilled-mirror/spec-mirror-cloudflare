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

[Scripts](https://developers.cloudflare.com/api/resources/workers/subresources/scripts)

[Assets](https://developers.cloudflare.com/api/resources/workers/subresources/scripts/subresources/assets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Upload

##### [Create Worker Assets Upload Session](https://developers.cloudflare.com/api/resources/workers/subresources/scripts/subresources/assets/subresources/upload/methods/create)

POST/accounts/{account\_id}/workers/scripts/{script\_name}/assets-upload-session

##### ModelsExpand Collapse

<details>

<summary>

UploadCreateResponse object { buckets, jwt }

</summary>

buckets: optional array of array of string

The requests to make to upload assets.

<a href="#">Link to this property</a>

jwt: optional string

A JWT to use as authentication for uploading assets.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.scripts.assets.upload%20%3E%20(model)%20upload_create_response%20%3E%20(schema)>)