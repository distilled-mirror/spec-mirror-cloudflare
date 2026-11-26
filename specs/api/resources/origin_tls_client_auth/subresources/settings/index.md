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

[Origin TLS Client Auth](https://developers.cloudflare.com/api/resources/origin_tls_client_auth)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Settings

##### [Get Enablement Setting for Zone](https://developers.cloudflare.com/api/resources/origin_tls_client_auth/subresources/settings/methods/get)

GET/zones/{zone\_id}/origin\_tls\_client\_auth/settings

##### [Set Enablement for Zone](https://developers.cloudflare.com/api/resources/origin_tls_client_auth/subresources/settings/methods/update)

PUT/zones/{zone\_id}/origin\_tls\_client\_auth/settings

##### ModelsExpand Collapse

<details>

<summary>

SettingGetResponse object { enabled }

</summary>

enabled: optional boolean

Indicates whether zone-level authenticated origin pulls is enabled.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20origin_tls_client_auth.settings%20%3E%20(model)%20setting_get_response%20%3E%20(schema)>)

<details>

<summary>

SettingUpdateResponse object { enabled }

</summary>

enabled: optional boolean

Indicates whether zone-level authenticated origin pulls is enabled.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20origin_tls_client_auth.settings%20%3E%20(model)%20setting_update_response%20%3E%20(schema)>)