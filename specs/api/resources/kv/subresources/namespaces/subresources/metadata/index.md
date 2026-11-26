---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Metadata
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[KV](https://developers.cloudflare.com/api/resources/kv)

[Namespaces](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Metadata

##### [Get a key's metadata](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces/subresources/metadata/methods/get)

GET/accounts/{account\_id}/storage/kv/namespaces/{namespace\_id}/metadata/{key\_name}

##### ModelsExpand Collapse

MetadataGetResponse = unknown

Arbitrary JSON that is associated with a key.

[Link to this property](#)%20kv.namespaces.metadata%20%3E%20(model)%20metadata_get_response%20%3E%20(schema)>)