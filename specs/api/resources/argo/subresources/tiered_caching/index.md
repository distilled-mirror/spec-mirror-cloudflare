---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Tiered Caching
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Argo](https://developers.cloudflare.com/api/resources/argo)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Tiered Caching

##### [Get Tiered Cache](https://developers.cloudflare.com/api/resources/argo/subresources/tiered_caching/methods/get)

GET/zones/{zone\_id}/argo/tiered\_caching

##### [Update Tiered Cache](https://developers.cloudflare.com/api/resources/argo/subresources/tiered_caching/methods/edit)

PATCH/zones/{zone\_id}/argo/tiered\_caching

##### ModelsExpand Collapse

<details>

<summary>

TieredCachingGetResponse object { id, editable, value, modified\_on }

</summary>

id: "tiered\_caching"

The identifier of the caching setting.

<a href="#">Link to this property</a>

editable: boolean

Whether the setting is editable.

<a href="#">Link to this property</a>

<details>

<summary>

value: "on" or "off"

Value of the Tiered Cache zone setting.

</summary>

One of the following:

"on"

<a href="#">Link to this property</a>

"off"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_on: optional string

Last time this setting was modified.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20argo.tiered_caching%20%3E%20(model)%20tiered_caching_get_response%20%3E%20(schema)>)

<details>

<summary>

TieredCachingEditResponse object { id, editable, value, modified\_on }

</summary>

id: "tiered\_caching"

The identifier of the caching setting.

<a href="#">Link to this property</a>

editable: boolean

Whether the setting is editable.

<a href="#">Link to this property</a>

<details>

<summary>

value: "on" or "off"

Value of the Tiered Cache zone setting.

</summary>

One of the following:

"on"

<a href="#">Link to this property</a>

"off"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_on: optional string

Last time this setting was modified.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20argo.tiered_caching%20%3E%20(model)%20tiered_caching_edit_response%20%3E%20(schema)>)