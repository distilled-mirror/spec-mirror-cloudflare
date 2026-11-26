---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Evaluation Types
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Evaluation Types

##### [List evaluator types (deprecated)](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/evaluation_types/methods/list)

GET/accounts/{account\_id}/ai-gateway/evaluation-types

##### ModelsExpand Collapse

<details>

<summary>

EvaluationTypeListResponse object { id, created\_at, description, 5 more }

</summary>

id: string

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: string

<a href="#">Link to this property</a>

enable: boolean

<a href="#">Link to this property</a>

mandatory: boolean

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.evaluation_types%20%3E%20(model)%20evaluation_type_list_response%20%3E%20(schema)>)