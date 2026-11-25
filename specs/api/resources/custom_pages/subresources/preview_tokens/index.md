---
agent:
  instructions: "This site offers a search API that returns relevant content across the entire site. Use the search endpoint to find information instead of crawling individual pages."
  search: "https://developers.cloudflare.com/.well-known/search?q={query}"
title: Preview Tokens
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Custom Pages](https://developers.cloudflare.com/api/resources/custom_pages)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

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