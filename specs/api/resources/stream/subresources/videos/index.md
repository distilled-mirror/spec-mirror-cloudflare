---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Videos
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Stream](https://developers.cloudflare.com/api/resources/stream)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Videos

##### [Storage use](https://developers.cloudflare.com/api/resources/stream/subresources/videos/methods/storage_usage)

GET/accounts/{account\_id}/stream/storage-usage

##### ModelsExpand Collapse

<details>

<summary>

VideoStorageUsageResponse object { creator, totalStorageMinutes, totalStorageMinutesLimit, videoCount }

</summary>

creator: optional string

A user-defined identifier for the media creator.

maxLength64

<a href="#">Link to this property</a>

totalStorageMinutes: optional number

The total minutes of video content stored in the account. May contain decimal values.

formatfloat

<a href="#">Link to this property</a>

totalStorageMinutesLimit: optional number

The storage capacity alloted for the account.

<a href="#">Link to this property</a>

videoCount: optional number

The total count of videos associated with the account.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20stream.videos%20%3E%20(model)%20video_storage_usage_response%20%3E%20(schema)>)