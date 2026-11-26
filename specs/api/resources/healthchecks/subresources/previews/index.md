---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Previews
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Healthchecks](https://developers.cloudflare.com/api/resources/healthchecks)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Previews

##### [Health Check Preview Details](https://developers.cloudflare.com/api/resources/healthchecks/subresources/previews/methods/get)

GET/zones/{zone\_id}/healthchecks/preview/{healthcheck\_id}

##### [Create Preview Health Check](https://developers.cloudflare.com/api/resources/healthchecks/subresources/previews/methods/create)

POST/zones/{zone\_id}/healthchecks/preview

##### [Delete Preview Health Check](https://developers.cloudflare.com/api/resources/healthchecks/subresources/previews/methods/delete)

DELETE/zones/{zone\_id}/healthchecks/preview/{healthcheck\_id}

##### ModelsExpand Collapse

<details>

<summary>

PreviewDeleteResponse object { id }

</summary>

id: optional string

Identifier

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20healthchecks.previews%20%3E%20(model)%20preview_delete_response%20%3E%20(schema)>)