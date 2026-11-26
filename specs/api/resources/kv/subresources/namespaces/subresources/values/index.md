---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Values
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[KV](https://developers.cloudflare.com/api/resources/kv)

[Namespaces](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Values

##### [Get a key's value](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces/subresources/values/methods/get)

GET/accounts/{account\_id}/storage/kv/namespaces/{namespace\_id}/values/{key\_name}

##### [Write a key-value pair with optional metadata](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces/subresources/values/methods/update)

PUT/accounts/{account\_id}/storage/kv/namespaces/{namespace\_id}/values/{key\_name}

##### [Delete a key-value pair](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces/subresources/values/methods/delete)

DELETE/accounts/{account\_id}/storage/kv/namespaces/{namespace\_id}/values/{key\_name}

##### ModelsExpand Collapse

ValueUpdateResponse object { }

[Link to this property](#)%20kv.namespaces.values%20%3E%20(model)%20value_update_response%20%3E%20(schema)>)

ValueDeleteResponse object { }

[Link to this property](#)%20kv.namespaces.values%20%3E%20(model)%20value_delete_response%20%3E%20(schema)>)