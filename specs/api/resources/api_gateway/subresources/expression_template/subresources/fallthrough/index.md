---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Fallthrough
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[API Gateway](https://developers.cloudflare.com/api/resources/api_gateway)

[Expression Template](https://developers.cloudflare.com/api/resources/api_gateway/subresources/expression_template)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Fallthrough

##### [Generate a fallthrough WAF expression template](https://developers.cloudflare.com/api/resources/api_gateway/subresources/expression_template/subresources/fallthrough/methods/create)

Deprecated

POST/zones/{zone\_id}/api\_gateway/expression-template/fallthrough

##### ModelsExpand Collapse

<details>

<summary>

FallthroughCreateResponse object { expression, title }

</summary>

expression: string

WAF Expression for fallthrough

<a href="#">Link to this property</a>

title: string

Title for the expression

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20api_gateway.expression_template.fallthrough%20%3E%20(model)%20fallthrough_create_response%20%3E%20(schema)>)