---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Account Profile
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Accounts](https://developers.cloudflare.com/api/resources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Account Profile

##### [Get account profile](https://developers.cloudflare.com/api/resources/accounts/subresources/account_profile/methods/get)

GET/accounts/{account\_id}/profile

##### [Update account profile](https://developers.cloudflare.com/api/resources/accounts/subresources/account_profile/methods/update)

PUT/accounts/{account\_id}/profile

##### ModelsExpand Collapse

<details>

<summary>

AccountProfile object { business\_address, business\_email, business\_name, 2 more }

</summary>

business\_address: string

<a href="#">Link to this property</a>

business\_email: string

<a href="#">Link to this property</a>

business\_name: string

<a href="#">Link to this property</a>

business\_phone: string

<a href="#">Link to this property</a>

external\_metadata: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.account_profile%20%3E%20(model)%20account_profile%20%3E%20(schema)>)