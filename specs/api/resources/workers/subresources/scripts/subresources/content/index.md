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

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Scripts](https://developers.cloudflare.com/api/resources/workers/subresources/scripts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Content

##### [Get Worker Script Content](https://developers.cloudflare.com/api/resources/workers/subresources/scripts/subresources/content/methods/get)

GET/accounts/{account\_id}/workers/scripts/{script\_name}/content/v2

##### [Replace Worker Script Content](https://developers.cloudflare.com/api/resources/workers/subresources/scripts/subresources/content/methods/update)

PUT/accounts/{account\_id}/workers/scripts/{script\_name}/content

##### ModelsExpand Collapse

ContentGetResponse = string

The script of a Worker in service worker syntax.

[Link to this property](#)%20workers.scripts.content%20%3E%20(model)%20content_get_response%20%3E%20(schema)>)