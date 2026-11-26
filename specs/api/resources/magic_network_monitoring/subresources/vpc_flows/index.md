---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: VPC Flows
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Magic Network Monitoring](https://developers.cloudflare.com/api/resources/magic_network_monitoring)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# VPC Flows

#### VPC FlowsTokens

##### [Generate authentication token for VPC flow logs export.](https://developers.cloudflare.com/api/resources/magic_network_monitoring/subresources/vpc_flows/subresources/tokens/methods/create)

POST/accounts/{account\_id}/mnm/vpc-flows/token

##### ModelsExpand Collapse

TokenCreateResponse = string

Authentication token to be used for VPC Flows export authentication.

[Link to this property](#)%20magic_network_monitoring.vpc_flows.tokens%20%3E%20(model)%20token_create_response%20%3E%20(schema)>)