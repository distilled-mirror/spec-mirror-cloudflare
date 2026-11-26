---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Settings
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Content Scanning](https://developers.cloudflare.com/api/resources/content_scanning)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Settings

##### [Get the Content Scanning status for a zone.](https://developers.cloudflare.com/api/resources/content_scanning/subresources/settings/methods/get)

GET/zones/{zone\_id}/content-upload-scan/settings

##### ModelsExpand Collapse

<details>

<summary>

SettingGetResponse object { modified, value }

Defines the status for Content Scanning.

</summary>

modified: optional string

Defines the last modification date (ISO 8601) of the Content Scanning status.

<a href="#">Link to this property</a>

value: optional string

Defines the status of Content Scanning.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20content_scanning.settings%20%3E%20(model)%20setting_get_response%20%3E%20(schema)>)