---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Logos
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Logos

##### [Create new saved logo queries from image files](https://developers.cloudflare.com/api/resources/brand_protection/subresources/logos/methods/create)

POST/accounts/{account\_id}/brand-protection/logos

##### [Delete saved logo queries by ID](https://developers.cloudflare.com/api/resources/brand_protection/subresources/logos/methods/delete)

DELETE/accounts/{account\_id}/brand-protection/logos/{logo\_id}

##### ModelsExpand Collapse

<details>

<summary>

LogoCreateResponse object { id, tag, upload\_path }

</summary>

id: optional number

<a href="#">Link to this property</a>

tag: optional string

<a href="#">Link to this property</a>

upload\_path: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.logos%20%3E%20(model)%20logo_create_response%20%3E%20(schema)>)