---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Passkeys
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Users](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/users)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Passkeys

##### [Delete a user's passkey](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/users/subresources/passkeys/methods/delete)

DELETE/accounts/{account\_id}/access/users/{user\_id}/passkeys/{authenticator\_id}

##### ModelsExpand Collapse

PasskeyDeleteResponse = unknown

[Link to this property](#)%20zero_trust.access.users.passkeys%20%3E%20(model)%20passkey_delete_response%20%3E%20(schema)>)