---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Vtt
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Stream](https://developers.cloudflare.com/api/resources/stream)

[Captions](https://developers.cloudflare.com/api/resources/stream/subresources/captions)

[Language](https://developers.cloudflare.com/api/resources/stream/subresources/captions/subresources/language)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Vtt

##### [Return WebVTT captions for a provided language](https://developers.cloudflare.com/api/resources/stream/subresources/captions/subresources/language/subresources/vtt/methods/get)

GET/accounts/{account\_id}/stream/{identifier}/captions/{language}/vtt

##### ModelsExpand Collapse

VttGetResponse = string

[Link to this property](#)%20stream.captions.language.vtt%20%3E%20(model)%20vtt_get_response%20%3E%20(schema)>)