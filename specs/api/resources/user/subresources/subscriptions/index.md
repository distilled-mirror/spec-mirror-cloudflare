---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Subscriptions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[User](https://developers.cloudflare.com/api/resources/user)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Subscriptions

##### [Get User Subscriptions](https://developers.cloudflare.com/api/resources/user/subresources/subscriptions/methods/get)

GET/user/subscriptions

##### [Update User Subscription](https://developers.cloudflare.com/api/resources/user/subresources/subscriptions/methods/update)

PUT/user/subscriptions/{identifier}

##### [Delete User Subscription](https://developers.cloudflare.com/api/resources/user/subresources/subscriptions/methods/delete)

DELETE/user/subscriptions/{identifier}

##### ModelsExpand Collapse

SubscriptionUpdateResponse = unknown

[Link to this property](#)%20user.subscriptions%20%3E%20(model)%20subscription_update_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionDeleteResponse object { subscription\_id }

</summary>

subscription\_id: optional string

Subscription identifier tag.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.subscriptions%20%3E%20(model)%20subscription_delete_response%20%3E%20(schema)>)