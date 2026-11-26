---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Prioritize
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Custom Certificates](https://developers.cloudflare.com/api/resources/custom_certificates)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Prioritize

##### [Re-prioritize SSL Certificates](https://developers.cloudflare.com/api/resources/custom_certificates/subresources/prioritize/methods/update)

PUT/zones/{zone\_id}/custom\_certificates/prioritize