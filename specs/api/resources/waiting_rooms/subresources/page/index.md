---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Page
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Waiting Rooms](https://developers.cloudflare.com/api/resources/waiting_rooms)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Page

##### [Create a custom waiting room page preview](https://developers.cloudflare.com/api/resources/waiting_rooms/subresources/page/methods/preview)

POST/zones/{zone\_id}/waiting\_rooms/preview

##### ModelsExpand Collapse

<details>

<summary>

PagePreviewResponse object { preview\_url }

</summary>

preview\_url: optional string

URL where the custom waiting room page can temporarily be previewed.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20waiting_rooms.page%20%3E%20(model)%20page_preview_response%20%3E%20(schema)>)