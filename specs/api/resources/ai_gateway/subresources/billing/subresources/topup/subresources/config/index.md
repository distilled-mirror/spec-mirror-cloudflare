---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Config
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

[Topup](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Config

##### [Get auto top-up configuration (deprecated)](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/subresources/config/methods/get)

Deprecated

GET/accounts/{account\_id}/ai-gateway/billing/topup/config

##### [Set auto top-up configuration](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/subresources/config/methods/create)

POST/accounts/{account\_id}/ai-gateway/billing/topup/config

##### [Delete auto top-up configuration](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/subresources/config/methods/delete)

DELETE/accounts/{account\_id}/ai-gateway/billing/topup/config

##### ModelsExpand Collapse

<details>

<summary>

ConfigGetResponse object { amount, threshold, disabledReason, 2 more }

</summary>

amount: number

Amount in cents that each auto top-up adds. 0 when auto top-up is off.

<a href="#">Link to this property</a>

threshold: number

Balance threshold in cents that triggers an auto top-up. 0 when auto top-up is off.

<a href="#">Link to this property</a>

disabledReason: optional string

Why auto top-up was stopped. Present only once it stopped.

<a href="#">Link to this property</a>

error: optional string

Message from the failure that stopped auto top-up. Present only once it stopped.

<a href="#">Link to this property</a>

lastFailedAt: optional number

When auto top-up was stopped, as a Unix timestamp in milliseconds. Present only once it stopped.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup.config%20%3E%20(model)%20config_get_response%20%3E%20(schema)>)

<details>

<summary>

ConfigCreateResponse = object { amount, threshold } or object { amount, status, threshold } or object { amount, client\_secret, setup\_intent\_id, 2 more }

</summary>

One of the following:

<details>

<summary>

object { amount, threshold }

</summary>

amount: number

Auto top-up amount in cents from the request.

<a href="#">Link to this property</a>

threshold: number

Balance threshold in cents from the request.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object { amount, status, threshold }

</summary>

amount: number

Auto top-up amount in cents from the request.

<a href="#">Link to this property</a>

status: "configured"

Auto top-up is saved.

<a href="#">Link to this property</a>

threshold: number

Balance threshold in cents from the request.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object { amount, client\_secret, setup\_intent\_id, 2 more }

</summary>

amount: number

Auto top-up amount in cents from the request.

<a href="#">Link to this property</a>

client\_secret: string

Client secret used to complete card authentication.

<a href="#">Link to this property</a>

setup\_intent\_id: string

Card setup identifier to send back as <code>setup_intent_id</code> once authenticated.

<a href="#">Link to this property</a>

status: "requires\_action"

The card must be authenticated with <code>client_secret</code> before auto top-up is saved. Then send the request again with <code>setup_intent_id</code>.

<a href="#">Link to this property</a>

threshold: number

Balance threshold in cents from the request.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup.config%20%3E%20(model)%20config_create_response%20%3E%20(schema)>)

ConfigDeleteResponse = unknown

[Link to this property](#)%20ai_gateway.billing.topup.config%20%3E%20(model)%20config_delete_response%20%3E%20(schema)>)