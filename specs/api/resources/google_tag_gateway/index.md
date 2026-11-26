---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Google Tag Gateway
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Google Tag Gateway

#### Google Tag GatewayConfig

##### [Get Google Tag Gateway configuration](https://developers.cloudflare.com/api/resources/google_tag_gateway/subresources/config/methods/get)

GET/zones/{zone\_id}/settings/google-tag-gateway/config

##### [Update Google Tag Gateway configuration](https://developers.cloudflare.com/api/resources/google_tag_gateway/subresources/config/methods/update)

PUT/zones/{zone\_id}/settings/google-tag-gateway/config

##### ModelsExpand Collapse

<details>

<summary>

Config object { enabled, endpoint, measurementId, 2 more }

Google Tag Gateway configuration for a zone.

</summary>

enabled: boolean

Enables or disables Google Tag Gateway for this zone.

<a href="#">Link to this property</a>

endpoint: string

Specifies the endpoint path for proxying Google Tag Manager requests. Use an absolute path starting with ’/’, with no nested paths and alphanumeric characters only (e.g. /metrics).

<a href="#">Link to this property</a>

measurementId: string

Specify the Google Tag Manager container or measurement ID (e.g. GTM-XXXXXXX or G-XXXXXXXXXX).

<a href="#">Link to this property</a>

DeprecatedhideOriginalIp: optional boolean

Deprecated. This value is stored but has no effect on traffic. Optional in requests: if omitted, the previously stored value is kept. Responses always include it.

<a href="#">Link to this property</a>

setUpTag: optional boolean

Set up the associated Google Tag on the zone automatically when enabled.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20google_tag_gateway.config%20%3E%20(model)%20config%20%3E%20(schema)>)