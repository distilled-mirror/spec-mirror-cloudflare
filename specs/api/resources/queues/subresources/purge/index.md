---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Purge
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Queues](https://developers.cloudflare.com/api/resources/queues)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Purge

##### [Get Queue Purge Status](https://developers.cloudflare.com/api/resources/queues/subresources/purge/methods/status)

GET/accounts/{account\_id}/queues/{queue\_id}/purge

##### [Purge Queue](https://developers.cloudflare.com/api/resources/queues/subresources/purge/methods/start)

POST/accounts/{account\_id}/queues/{queue\_id}/purge

##### ModelsExpand Collapse

<details>

<summary>

PurgeStatusResponse object { completed, started\_at }

</summary>

completed: optional string

Indicates if the last purge operation completed successfully.

<a href="#">Link to this property</a>

started\_at: optional string

Timestamp when the last purge operation started.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20queues.purge%20%3E%20(model)%20purge_status_response%20%3E%20(schema)>)