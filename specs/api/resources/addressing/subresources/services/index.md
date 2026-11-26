---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Services
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Addressing](https://developers.cloudflare.com/api/resources/addressing)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Services

##### [List Services](https://developers.cloudflare.com/api/resources/addressing/subresources/services/methods/list)

GET/accounts/{account\_id}/addressing/services

##### ModelsExpand Collapse

<details>

<summary>

ServiceListResponse object { id, name }

</summary>

id: optional string

Identifier of a Service on the Cloudflare network. Available services and their IDs may be found in the **List Services** endpoint.

maxLength32

<a href="#">Link to this property</a>

name: optional string

Name of a service running on the Cloudflare network

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20addressing.services%20%3E%20(model)%20service_list_response%20%3E%20(schema)>)