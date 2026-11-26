---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Hosts
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[API Gateway](https://developers.cloudflare.com/api/resources/api_gateway)

[User Schemas](https://developers.cloudflare.com/api/resources/api_gateway/subresources/user_schemas)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Hosts

##### [Retrieve schema hosts in a zone](https://developers.cloudflare.com/api/resources/api_gateway/subresources/user_schemas/subresources/hosts/methods/list)

Deprecated

GET/zones/{zone\_id}/api\_gateway/user\_schemas/hosts

##### ModelsExpand Collapse

<details>

<summary>

HostListResponse object { created\_at, hosts, name, schema\_id }

</summary>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

hosts: array of string

Hosts serving the schema, e.g zone.host.com

<a href="#">Link to this property</a>

name: string

Name of the schema

<a href="#">Link to this property</a>

schema\_id: string

UUID.

maxLength36

minLength36

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20api_gateway.user_schemas.hosts%20%3E%20(model)%20host_list_response%20%3E%20(schema)>)