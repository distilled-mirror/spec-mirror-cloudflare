---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Ownership
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Logpush](https://developers.cloudflare.com/api/resources/logpush)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Ownership

##### [Get ownership challenge](https://developers.cloudflare.com/api/resources/logpush/subresources/ownership/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/logpush/ownership

##### [Validate ownership challenge](https://developers.cloudflare.com/api/resources/logpush/subresources/ownership/methods/validate)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/logpush/ownership/validate

##### ModelsExpand Collapse

<details>

<summary>

OwnershipValidation object { valid }

</summary>

valid: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20logpush.ownership%20%3E%20(model)%20ownership_validation%20%3E%20(schema)>)

<details>

<summary>

OwnershipCreateResponse object { filename, message, valid }

</summary>

filename: optional string

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

valid: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20logpush.ownership%20%3E%20(model)%20ownership_create_response%20%3E%20(schema)>)