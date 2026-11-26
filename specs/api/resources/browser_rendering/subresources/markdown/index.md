---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Markdown
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Markdown

##### [Get markdown.](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/markdown/methods/create)

POST/accounts/{account\_id}/browser-rendering/markdown

##### ModelsExpand Collapse

MarkdownCreateResponse = string

Markdown content. Prefixed with YAML frontmatter (e.g. `title`) when the page provides that metadata.

[Link to this property](#)%20browser_rendering.markdown%20%3E%20(model)%20markdown_create_response%20%3E%20(schema)>)