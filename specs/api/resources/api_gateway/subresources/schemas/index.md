---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Schemas
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[API Gateway](https://developers.cloudflare.com/api/resources/api_gateway)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Schemas

##### [Export web and API operations as OpenAPI schemas](https://developers.cloudflare.com/api/resources/api_gateway/subresources/schemas/methods/list)

GET/zones/{zone\_id}/api\_gateway/schemas

##### ModelsExpand Collapse

<details>

<summary>

SchemaListResponse object { schemas, timestamp }

</summary>

schemas: optional array of unknown

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20api_gateway.schemas%20%3E%20(model)%20schema_list_response%20%3E%20(schema)>)