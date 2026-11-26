---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Protocols
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Spectrum](https://developers.cloudflare.com/api/resources/spectrum)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Protocols

##### [List Spectrum application protocols](https://developers.cloudflare.com/api/resources/spectrum/subresources/protocols/methods/list)

GET/zones/{zone\_id}/spectrum/protocols

##### ModelsExpand Collapse

<details>

<summary>

ProtocolListResponse object { description, name, ports, transport }

</summary>

description: string

The full name of the application protocol.

<a href="#">Link to this property</a>

name: string

The short name of the application protocol.

<a href="#">Link to this property</a>

ports: array of number

The available listening ports for the given protocol.

<a href="#">Link to this property</a>

transport: string

The transport layer protocol used by the application protocol

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20spectrum.protocols%20%3E%20(model)%20protocol_list_response%20%3E%20(schema)>)