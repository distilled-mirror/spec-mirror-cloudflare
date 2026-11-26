---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Patterns
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[DLP](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Patterns

##### [Validate a DLP regex pattern](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/patterns/methods/validate)

POST/accounts/{account\_id}/dlp/patterns/validate

##### ModelsExpand Collapse

<details>

<summary>

PatternValidateResponse object { valid }

</summary>

valid: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.patterns%20%3E%20(model)%20pattern_validate_response%20%3E%20(schema)>)