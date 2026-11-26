---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Preview Tokens
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Custom Pages](https://developers.cloudflare.com/api/resources/custom_pages)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Preview Tokens

##### [Create a preview token](https://developers.cloudflare.com/api/resources/custom_pages/subresources/preview_tokens/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/custom\_pages/preview\_tokens

##### ModelsExpand Collapse

<details>

<summary>

PreviewTokenCreateResponse object { cep\_jwt }

</summary>

cep\_jwt: string

A signed JWT token used to authenticate the preview request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20custom_pages.preview_tokens%20%3E%20(model)%20preview_token_create_response%20%3E%20(schema)>)