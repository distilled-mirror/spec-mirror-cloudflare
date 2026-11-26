---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Status
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[DDoS Protection](https://developers.cloudflare.com/api/resources/ddos_protection)

[Advanced TCP Protection](https://developers.cloudflare.com/api/resources/ddos_protection/subresources/advanced_tcp_protection)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Status

##### [Get protection status.](https://developers.cloudflare.com/api/resources/ddos_protection/subresources/advanced_tcp_protection/subresources/status/methods/get)

GET/accounts/{account\_id}/magic/advanced\_tcp\_protection/configs/tcp\_protection\_status

##### [Update protection status.](https://developers.cloudflare.com/api/resources/ddos_protection/subresources/advanced_tcp_protection/subresources/status/methods/edit)

PATCH/accounts/{account\_id}/magic/advanced\_tcp\_protection/configs/tcp\_protection\_status

##### ModelsExpand Collapse

<details>

<summary>

StatusGetResponse object { enabled }

</summary>

enabled: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ddos_protection.advanced_tcp_protection.status%20%3E%20(model)%20status_get_response%20%3E%20(schema)>)

<details>

<summary>

StatusEditResponse object { enabled }

</summary>

enabled: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ddos_protection.advanced_tcp_protection.status%20%3E%20(model)%20status_edit_response%20%3E%20(schema)>)