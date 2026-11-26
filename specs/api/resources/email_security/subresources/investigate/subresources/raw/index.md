---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Raw
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Email Security](https://developers.cloudflare.com/api/resources/email_security)

[Investigate](https://developers.cloudflare.com/api/resources/email_security/subresources/investigate)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Raw

##### [Get raw email content](https://developers.cloudflare.com/api/resources/email_security/subresources/investigate/subresources/raw/methods/get)

GET/accounts/{account\_id}/email-security/investigate/{investigate\_id}/raw

##### ModelsExpand Collapse

<details>

<summary>

RawGetResponse object { raw }

</summary>

raw: string

A UTF-8 encoded eml file of the email.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20email_security.investigate.raw%20%3E%20(model)%20raw_get_response%20%3E%20(schema)>)