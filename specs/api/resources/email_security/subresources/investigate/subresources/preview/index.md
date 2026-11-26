---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Preview
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Email Security](https://developers.cloudflare.com/api/resources/email_security)

[Investigate](https://developers.cloudflare.com/api/resources/email_security/subresources/investigate)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Preview

##### [Get preview for a detection](https://developers.cloudflare.com/api/resources/email_security/subresources/investigate/subresources/preview/methods/get)

GET/accounts/{account\_id}/email-security/investigate/{investigate\_id}/preview

##### [Generate preview for a non-detection message](https://developers.cloudflare.com/api/resources/email_security/subresources/investigate/subresources/preview/methods/create)

POST/accounts/{account\_id}/email-security/investigate/preview

##### ModelsExpand Collapse

<details>

<summary>

PreviewGetResponse object { screenshot }

</summary>

screenshot: string

A base64 encoded PNG image of the email.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20email_security.investigate.preview%20%3E%20(model)%20preview_get_response%20%3E%20(schema)>)

<details>

<summary>

PreviewCreateResponse object { screenshot }

</summary>

screenshot: string

A base64 encoded PNG image of the email.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20email_security.investigate.preview%20%3E%20(model)%20preview_create_response%20%3E%20(schema)>)