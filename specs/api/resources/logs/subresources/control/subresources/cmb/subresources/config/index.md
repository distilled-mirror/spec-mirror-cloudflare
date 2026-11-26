---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Config
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Logs](https://developers.cloudflare.com/api/resources/logs)

[Control](https://developers.cloudflare.com/api/resources/logs/subresources/control)

[Cmb](https://developers.cloudflare.com/api/resources/logs/subresources/control/subresources/cmb)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Config

##### [Get CMB config](https://developers.cloudflare.com/api/resources/logs/subresources/control/subresources/cmb/subresources/config/methods/get)

GET/accounts/{account\_id}/logs/control/cmb/config

##### [Update CMB config](https://developers.cloudflare.com/api/resources/logs/subresources/control/subresources/cmb/subresources/config/methods/create)

POST/accounts/{account\_id}/logs/control/cmb/config

##### [Delete CMB config](https://developers.cloudflare.com/api/resources/logs/subresources/control/subresources/cmb/subresources/config/methods/delete)

DELETE/accounts/{account\_id}/logs/control/cmb/config

##### ModelsExpand Collapse

<details>

<summary>

CmbConfig object { allow\_out\_of\_region\_access, regions }

</summary>

allow\_out\_of\_region\_access: optional boolean

Allow out of region access

<a href="#">Link to this property</a>

regions: optional string

Name of the region.

maxLength256

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20logs.control.cmb.config%20%3E%20(model)%20cmb_config%20%3E%20(schema)>)

ConfigDeleteResponse = unknown

[Link to this property](#)%20logs.control.cmb.config%20%3E%20(model)%20config_delete_response%20%3E%20(schema)>)