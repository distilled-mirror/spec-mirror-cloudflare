---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Client Secret
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Accounts](https://developers.cloudflare.com/api/resources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Client Secret

##### [Create Setup Intent](https://developers.cloudflare.com/api/resources/accounts/subresources/client_secret/methods/create)

POST/accounts/{account\_id}/client-secret

##### ModelsExpand Collapse

<details>

<summary>

ClientSecretCreateResponse object { client\_secret }

</summary>

client\_secret: optional string

The Stripe client secret for frontend payment confirmation.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.client_secret%20%3E%20(model)%20client_secret_create_response%20%3E%20(schema)>)