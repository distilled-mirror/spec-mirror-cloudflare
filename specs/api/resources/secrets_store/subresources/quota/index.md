---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Quota
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Secrets Store](https://developers.cloudflare.com/api/resources/secrets_store)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Quota

##### [View secret usage](https://developers.cloudflare.com/api/resources/secrets_store/subresources/quota/methods/get)

GET/accounts/{account\_id}/secrets\_store/quota

##### ModelsExpand Collapse

<details>

<summary>

QuotaGetResponse object { secrets }

</summary>

<details>

<summary>

secrets: object { quota, usage }

</summary>

quota: number

The number of secrets the account is entitled to use.

<a href="#">Link to this property</a>

usage: number

The number of secrets the account is currently using.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20secrets_store.quota%20%3E%20(model)%20quota_get_response%20%3E%20(schema)>)