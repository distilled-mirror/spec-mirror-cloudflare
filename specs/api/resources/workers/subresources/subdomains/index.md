---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Subdomains
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Subdomains

##### [Get a Workers Subdomain](https://developers.cloudflare.com/api/resources/workers/subresources/subdomains/methods/get)

GET/accounts/{account\_id}/workers/subdomain

##### [Create a Workers Subdomain](https://developers.cloudflare.com/api/resources/workers/subresources/subdomains/methods/update)

PUT/accounts/{account\_id}/workers/subdomain

##### [Delete Workers Subdomain](https://developers.cloudflare.com/api/resources/workers/subresources/subdomains/methods/delete)

DELETE/accounts/{account\_id}/workers/subdomain

##### ModelsExpand Collapse

<details>

<summary>

SubdomainGetResponse object { subdomain }

</summary>

subdomain: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.subdomains%20%3E%20(model)%20subdomain_get_response%20%3E%20(schema)>)

<details>

<summary>

SubdomainUpdateResponse object { subdomain }

</summary>

subdomain: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.subdomains%20%3E%20(model)%20subdomain_update_response%20%3E%20(schema)>)