---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Delegations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Addressing](https://developers.cloudflare.com/api/resources/addressing)

[Prefixes](https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Delegations

##### [List Prefix Delegations](https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/delegations/methods/list)

GET/accounts/{account\_id}/addressing/prefixes/{prefix\_id}/delegations

##### [Create Prefix Delegation](https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/delegations/methods/create)

POST/accounts/{account\_id}/addressing/prefixes/{prefix\_id}/delegations

##### [Delete Prefix Delegation](https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/delegations/methods/delete)

DELETE/accounts/{account\_id}/addressing/prefixes/{prefix\_id}/delegations/{delegation\_id}

##### ModelsExpand Collapse

<details>

<summary>

Delegations object { id, cidr, created\_at, 3 more }

</summary>

id: optional string

Identifier of a Delegation.

maxLength32

<a href="#">Link to this property</a>

cidr: optional string

IP Prefix in Classless Inter-Domain Routing format.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

delegated\_account\_id: optional string

Account identifier for the account to which prefix is being delegated.

maxLength32

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

parent\_prefix\_id: optional string

Identifier of an IP Prefix.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20addressing.prefixes.delegations%20%3E%20(model)%20delegations%20%3E%20(schema)>)

<details>

<summary>

DelegationDeleteResponse object { id }

</summary>

id: optional string

Identifier of a Delegation.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20addressing.prefixes.delegations%20%3E%20(model)%20delegation_delete_response%20%3E%20(schema)>)