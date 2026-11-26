---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: By Dataset
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Events](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events)

[Target Industries](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/target_industries)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# By Dataset

##### [List target industries in a dataset (legacy)](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/target_industries/subresources/by_dataset/methods/list)

GET/accounts/{account\_id}/cloudforce-one/events/dataset/{dataset\_id}/targetIndustries

##### ModelsExpand Collapse

<details>

<summary>

ByDatasetListResponse object { items, type }

</summary>

<details>

<summary>

items: object { type }

</summary>

type: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.target_industries.by_dataset%20%3E%20(model)%20by_dataset_list_response%20%3E%20(schema)>)