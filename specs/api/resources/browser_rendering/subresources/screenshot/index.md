---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Screenshot
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Screenshot

##### [Get screenshot.](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/screenshot/methods/create)

POST/accounts/{account\_id}/browser-rendering/screenshot

##### ModelsExpand Collapse

<details>

<summary>

ScreenshotCreateResponse object { success, errors }

</summary>

success: boolean

Response status.

<a href="#">Link to this property</a>

<details>

<summary>

errors: optional array of object { code, message }

</summary>

code: number

Error code.

<a href="#">Link to this property</a>

message: string

Error message.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.screenshot%20%3E%20(model)%20screenshot_create_response%20%3E%20(schema)>)