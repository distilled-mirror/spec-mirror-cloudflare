---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Direct Uploads
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Images](https://developers.cloudflare.com/api/resources/images)

[V2](https://developers.cloudflare.com/api/resources/images/subresources/v2)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Direct Uploads

##### [Create authenticated direct upload URL V2](https://developers.cloudflare.com/api/resources/images/subresources/v2/subresources/direct_uploads/methods/create)

POST/accounts/{account\_id}/images/v2/direct\_upload

##### ModelsExpand Collapse

<details>

<summary>

DirectUploadCreateResponse object { id, uploadURL }

</summary>

id: optional string

Image unique identifier.

maxLength32

<a href="#">Link to this property</a>

uploadURL: optional string

The URL the unauthenticated upload can be performed to using a single HTTP POST (multipart/form-data) request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20images.v2.direct_uploads%20%3E%20(model)%20direct_upload_create_response%20%3E%20(schema)>)