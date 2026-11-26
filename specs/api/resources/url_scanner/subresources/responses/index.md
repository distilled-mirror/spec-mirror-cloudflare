---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Responses
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[URL Scanner](https://developers.cloudflare.com/api/resources/url_scanner)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Responses

##### [Get raw response](https://developers.cloudflare.com/api/resources/url_scanner/subresources/responses/methods/get)

GET/accounts/{account\_id}/urlscanner/v2/responses/{response\_id}

##### ModelsExpand Collapse

ResponseGetResponse = string

Web resource or image.

[Link to this property](#)%20url_scanner.responses%20%3E%20(model)%20response_get_response%20%3E%20(schema)>)