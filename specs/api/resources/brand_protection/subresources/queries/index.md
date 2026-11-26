---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Queries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Queries

##### [Create new saved string queries](https://developers.cloudflare.com/api/resources/brand_protection/subresources/queries/methods/create)

POST/accounts/{account\_id}/brand-protection/queries

##### [Delete saved string queries by ID](https://developers.cloudflare.com/api/resources/brand_protection/subresources/queries/methods/delete)

DELETE/accounts/{account\_id}/brand-protection/queries

##### [Create new saved string queries in bulk](https://developers.cloudflare.com/api/resources/brand_protection/subresources/queries/methods/bulk)

POST/accounts/{account\_id}/brand-protection/queries/bulk