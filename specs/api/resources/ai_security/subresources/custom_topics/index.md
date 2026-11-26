---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Custom Topics
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Security](https://developers.cloudflare.com/api/resources/ai_security)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Custom Topics

##### [Get the AI Security for Apps custom topics of a zone.](https://developers.cloudflare.com/api/resources/ai_security/subresources/custom_topics/methods/get)

GET/zones/{zone\_id}/ai-security/custom-topics

##### [Update the AI Security for Apps custom topics of a zone.](https://developers.cloudflare.com/api/resources/ai_security/subresources/custom_topics/methods/update)

PUT/zones/{zone\_id}/ai-security/custom-topics

##### ModelsExpand Collapse

<details>

<summary>

CustomTopicGetResponse object { topics }

</summary>

<details>

<summary>

topics: optional array of object { label, topic }

Custom topic categories for AI Security for Apps content detection.

</summary>

label: string

Unique label identifier. Must contain only lowercase letters (a–z), digits (0–9), and hyphens.

maxLength20

minLength2

<a href="#">Link to this property</a>

topic: string

Description of the topic category. Must contain 2–50 UTF-8 bytes. Text in any language is supported, including spaces, numbers, punctuation, and symbols. Tabs, line breaks, invalid text, and invisible formatting characters are not allowed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_security.custom_topics%20%3E%20(model)%20custom_topic_get_response%20%3E%20(schema)>)

<details>

<summary>

CustomTopicUpdateResponse object { topics }

</summary>

<details>

<summary>

topics: optional array of object { label, topic }

Custom topic categories for AI Security for Apps content detection.

</summary>

label: string

Unique label identifier. Must contain only lowercase letters (a–z), digits (0–9), and hyphens.

maxLength20

minLength2

<a href="#">Link to this property</a>

topic: string

Description of the topic category. Must contain 2–50 UTF-8 bytes. Text in any language is supported, including spaces, numbers, punctuation, and symbols. Tabs, line breaks, invalid text, and invisible formatting characters are not allowed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_security.custom_topics%20%3E%20(model)%20custom_topic_update_response%20%3E%20(schema)>)