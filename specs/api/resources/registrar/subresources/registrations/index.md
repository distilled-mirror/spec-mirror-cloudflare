---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Registrations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Registrar](https://developers.cloudflare.com/api/resources/registrar)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Registrations

##### [Create Registration](https://developers.cloudflare.com/api/resources/registrar/subresources/registrations/methods/create)

POST/accounts/{account\_id}/registrar/registrations

##### [List Registrations](https://developers.cloudflare.com/api/resources/registrar/subresources/registrations/methods/list)

GET/accounts/{account\_id}/registrar/registrations

##### [Get Registration](https://developers.cloudflare.com/api/resources/registrar/subresources/registrations/methods/get)

GET/accounts/{account\_id}/registrar/registrations/{domain\_name}

##### [Update Registration](https://developers.cloudflare.com/api/resources/registrar/subresources/registrations/methods/edit)

PATCH/accounts/{account\_id}/registrar/registrations/{domain\_name}