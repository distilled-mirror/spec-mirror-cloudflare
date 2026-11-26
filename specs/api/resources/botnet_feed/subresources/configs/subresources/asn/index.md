---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: ASN
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Botnet Feed](https://developers.cloudflare.com/api/resources/botnet_feed)

[Configs](https://developers.cloudflare.com/api/resources/botnet_feed/subresources/configs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# ASN

##### [Get list of ASNs](https://developers.cloudflare.com/api/resources/botnet_feed/subresources/configs/subresources/asn/methods/get)

GET/accounts/{account\_id}/botnet\_feed/configs/asn

##### [Delete an ASN](https://developers.cloudflare.com/api/resources/botnet_feed/subresources/configs/subresources/asn/methods/delete)

DELETE/accounts/{account\_id}/botnet\_feed/configs/asn/{asn\_id}

##### ModelsExpand Collapse

<details>

<summary>

ASNGetResponse object { asn }

</summary>

asn: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20botnet_feed.configs.asn%20%3E%20(model)%20asn_get_response%20%3E%20(schema)>)

<details>

<summary>

ASNDeleteResponse object { asn }

</summary>

asn: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20botnet_feed.configs.asn%20%3E%20(model)%20asn_delete_response%20%3E%20(schema)>)