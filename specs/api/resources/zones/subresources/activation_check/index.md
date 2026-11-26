---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Activation Check
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zones](https://developers.cloudflare.com/api/resources/zones)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Activation Check

##### [Rerun the Activation Check](https://developers.cloudflare.com/api/resources/zones/subresources/activation_check/methods/trigger)

PUT/zones/{zone\_id}/activation\_check

##### ModelsExpand Collapse

<details>

<summary>

ActivationCheckTriggerResponse object { id }

</summary>

id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.activation_check%20%3E%20(model)%20activation_check_trigger_response%20%3E%20(schema)>)