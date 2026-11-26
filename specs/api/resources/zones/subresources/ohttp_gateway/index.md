---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Ohttp Gateway
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zones](https://developers.cloudflare.com/api/resources/zones)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Ohttp Gateway

##### [Get OHTTP Gateway enablement](https://developers.cloudflare.com/api/resources/zones/subresources/ohttp_gateway/methods/get)

GET/zones/{zone\_id}/settings/ohttp-gateway

##### [Enable OHTTP Gateway](https://developers.cloudflare.com/api/resources/zones/subresources/ohttp_gateway/methods/create)

PUT/zones/{zone\_id}/settings/ohttp-gateway

##### [Disable OHTTP Gateway](https://developers.cloudflare.com/api/resources/zones/subresources/ohttp_gateway/methods/delete)

DELETE/zones/{zone\_id}/settings/ohttp-gateway

##### ModelsExpand Collapse

<details>

<summary>

OhttpGatewayGetResponse = "on" or "off"

</summary>

One of the following:

"on"

<a href="#">Link to this property</a>

"off"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.ohttp_gateway%20%3E%20(model)%20ohttp_gateway_get_response%20%3E%20(schema)>)

<details>

<summary>

OhttpGatewayCreateResponse = "on" or "off"

</summary>

One of the following:

"on"

<a href="#">Link to this property</a>

"off"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.ohttp_gateway%20%3E%20(model)%20ohttp_gateway_create_response%20%3E%20(schema)>)

<details>

<summary>

OhttpGatewayDeleteResponse = "on" or "off"

</summary>

One of the following:

"on"

<a href="#">Link to this property</a>

"off"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.ohttp_gateway%20%3E%20(model)%20ohttp_gateway_delete_response%20%3E%20(schema)>)