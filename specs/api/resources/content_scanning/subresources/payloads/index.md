---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Payloads
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Content Scanning](https://developers.cloudflare.com/api/resources/content_scanning)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Payloads

##### [List the Content Scanning custom expressions of a zone.](https://developers.cloudflare.com/api/resources/content_scanning/subresources/payloads/methods/list)

GET/zones/{zone\_id}/content-upload-scan/payloads

##### [Create Content Scanning custom expressions for a zone.](https://developers.cloudflare.com/api/resources/content_scanning/subresources/payloads/methods/create)

POST/zones/{zone\_id}/content-upload-scan/payloads

##### [Delete a Content Scanning custom expression from a zone.](https://developers.cloudflare.com/api/resources/content_scanning/subresources/payloads/methods/delete)

DELETE/zones/{zone\_id}/content-upload-scan/payloads/{expression\_id}

##### [Update a Content Scanning custom expression for a zone.](https://developers.cloudflare.com/api/resources/content_scanning/subresources/payloads/methods/update)

PATCH/zones/{zone\_id}/content-upload-scan/payloads/{expression\_id}

##### ModelsExpand Collapse

<details>

<summary>

PayloadListResponse object { id, payload }

Defines a Content Scanning custom expression.

</summary>

id: optional string

Defines the unique ID for this Content Scanning custom expression.

maxLength32

<a href="#">Link to this property</a>

payload: optional string

Defines the custom content extraction expression used to reach content objects in the request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20content_scanning.payloads%20%3E%20(model)%20payload_list_response%20%3E%20(schema)>)

<details>

<summary>

PayloadCreateResponse object { id, payload }

Defines a Content Scanning custom expression.

</summary>

id: optional string

Defines the unique ID for this Content Scanning custom expression.

maxLength32

<a href="#">Link to this property</a>

payload: optional string

Defines the custom content extraction expression used to reach content objects in the request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20content_scanning.payloads%20%3E%20(model)%20payload_create_response%20%3E%20(schema)>)

<details>

<summary>

PayloadDeleteResponse object { id, payload }

Defines a Content Scanning custom expression.

</summary>

id: optional string

Defines the unique ID for this Content Scanning custom expression.

maxLength32

<a href="#">Link to this property</a>

payload: optional string

Defines the custom content extraction expression used to reach content objects in the request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20content_scanning.payloads%20%3E%20(model)%20payload_delete_response%20%3E%20(schema)>)

<details>

<summary>

PayloadUpdateResponse object { id, payload }

Defines a Content Scanning custom expression.

</summary>

id: optional string

Defines the unique ID for this Content Scanning custom expression.

maxLength32

<a href="#">Link to this property</a>

payload: optional string

Defines the custom content extraction expression used to reach content objects in the request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20content_scanning.payloads%20%3E%20(model)%20payload_update_response%20%3E%20(schema)>)