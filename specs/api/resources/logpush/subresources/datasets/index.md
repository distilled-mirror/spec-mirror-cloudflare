---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Datasets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Logpush](https://developers.cloudflare.com/api/resources/logpush)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Datasets

#### DatasetsFields

##### [List fields](https://developers.cloudflare.com/api/resources/logpush/subresources/datasets/subresources/fields/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/logpush/datasets/{dataset\_id}/fields

##### ModelsExpand Collapse

FieldGetResponse = map\[string]

[Link to this property](#)%20logpush.datasets.fields%20%3E%20(model)%20field_get_response%20%3E%20(schema)>)

#### DatasetsJobs

##### [List Logpush jobs for a dataset](https://developers.cloudflare.com/api/resources/logpush/subresources/datasets/subresources/jobs/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/logpush/datasets/{dataset\_id}/jobs