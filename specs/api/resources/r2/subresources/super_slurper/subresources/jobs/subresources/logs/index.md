---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Logs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Super Slurper](https://developers.cloudflare.com/api/resources/r2/subresources/super_slurper)

[Jobs](https://developers.cloudflare.com/api/resources/r2/subresources/super_slurper/subresources/jobs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Logs

##### [Get job logs](https://developers.cloudflare.com/api/resources/r2/subresources/super_slurper/subresources/jobs/subresources/logs/methods/list)

GET/accounts/{account\_id}/slurper/jobs/{job\_id}/logs

##### ModelsExpand Collapse

<details>

<summary>

LogListResponse object { createdAt, job, logType, 2 more }

</summary>

createdAt: optional string

<a href="#">Link to this property</a>

job: optional string

<a href="#">Link to this property</a>

<details>

<summary>

logType: optional "migrationStart" or "migrationComplete" or "migrationAbort" or 12 more

</summary>

One of the following:

"migrationStart"

<a href="#">Link to this property</a>

"migrationComplete"

<a href="#">Link to this property</a>

"migrationAbort"

<a href="#">Link to this property</a>

"migrationError"

<a href="#">Link to this property</a>

"migrationPause"

<a href="#">Link to this property</a>

"migrationResume"

<a href="#">Link to this property</a>

"migrationErrorFailedContinuation"

<a href="#">Link to this property</a>

"importErrorRetryExhaustion"

<a href="#">Link to this property</a>

"importSkippedStorageClass"

<a href="#">Link to this property</a>

"importSkippedOversized"

<a href="#">Link to this property</a>

"importSkippedEmptyObject"

<a href="#">Link to this property</a>

"importSkippedUnsupportedContentType"

<a href="#">Link to this property</a>

"importSkippedExcludedContentType"

<a href="#">Link to this property</a>

"importSkippedInvalidMedia"

<a href="#">Link to this property</a>

"importSkippedRequiresRetrieval"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

objectKey: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.super_slurper.jobs.logs%20%3E%20(model)%20log_list_response%20%3E%20(schema)>)