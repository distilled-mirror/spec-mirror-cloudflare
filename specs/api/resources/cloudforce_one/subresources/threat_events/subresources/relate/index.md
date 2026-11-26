---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Relate
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Events](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Relate

##### [Remove event references (legacy)](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/relate/methods/delete)

DELETE/accounts/{account\_id}/cloudforce-one/events/relate/{event\_id}

##### ModelsExpand Collapse

<details>

<summary>

RelateDeleteResponse object { success }

</summary>

success: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.relate%20%3E%20(model)%20relate_delete_response%20%3E%20(schema)>)