---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Pay Invoice
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Accounts](https://developers.cloudflare.com/api/resources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Pay Invoice

##### [Pay Invoice](https://developers.cloudflare.com/api/resources/accounts/subresources/pay_invoice/methods/create)

POST/accounts/{account\_id}/pay-invoice

##### ModelsExpand Collapse

<details>

<summary>

PayInvoiceCreateResponse object { client\_secret }

</summary>

client\_secret: optional string

The Stripe client secret for frontend payment confirmation.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.pay_invoice%20%3E%20(model)%20pay_invoice_create_response%20%3E%20(schema)>)