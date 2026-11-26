---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Account Settings
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Account Settings

##### [Fetch Workers Account Settings](https://developers.cloudflare.com/api/resources/workers/subresources/account_settings/methods/get)

GET/accounts/{account\_id}/workers/account-settings

##### [Configure Workers Account Settings](https://developers.cloudflare.com/api/resources/workers/subresources/account_settings/methods/update)

PUT/accounts/{account\_id}/workers/account-settings

##### ModelsExpand Collapse

<details>

<summary>

AccountSettingGetResponse object { default\_usage\_model, green\_compute }

</summary>

default\_usage\_model: optional string

<a href="#">Link to this property</a>

green\_compute: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.account_settings%20%3E%20(model)%20account_setting_get_response%20%3E%20(schema)>)

<details>

<summary>

AccountSettingUpdateResponse object { default\_usage\_model, green\_compute }

</summary>

default\_usage\_model: optional string

<a href="#">Link to this property</a>

green\_compute: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.account_settings%20%3E%20(model)%20account_setting_update_response%20%3E%20(schema)>)