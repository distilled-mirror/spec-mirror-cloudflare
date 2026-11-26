---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Results
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Scans](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/scans)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Results

##### [Get the Latest Scan Result](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/scans/subresources/results/methods/get)

GET/accounts/{account\_id}/cloudforce-one/scans/results/{config\_id}

##### ModelsExpand Collapse

<details>

<summary>

ScanResult object { number, proto, status }

</summary>

number: optional number

<a href="#">Link to this property</a>

proto: optional string

<a href="#">Link to this property</a>

status: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.scans.results%20%3E%20(model)%20scan_result%20%3E%20(schema)>)

<details>

<summary>

ResultGetResponse object { "1.1.1.1" }

</summary>

<details>

<summary>

"1.1.1.1": array of <a href="https://developers.cloudflare.com/api/resources/cloudforce_one#(resource)%20cloudforce_one.scans.results%20%3E%20(model)%20scan_result%20%3E%20(schema)">ScanResult</a> { number, proto, status }

</summary>

number: optional number

<a href="#">Link to this property</a>

proto: optional string

<a href="#">Link to this property</a>

status: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.scans.results%20%3E%20(model)%20result_get_response%20%3E%20(schema)>)