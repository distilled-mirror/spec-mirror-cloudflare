---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Get credit balance
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Get credit balance

GET/accounts/{account\_id}/ai-gateway/billing/credit-balance

Retrieve the current credit balance, payment method info, and top-up configuration.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### Accepted Permissions (at least one required)

`AI Gateway Metadata Read` `AI Search Index Engine` `Auto Rag Write Run Engine` `AI Gateway Write` `AI Gateway Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { balance, has\_default\_payment\_method, payment\_method, 2 more }

</summary>

balance: number

Credit balance in US cents. Can be fractional, because usage is deducted in fractions of a cent, and is negative when usage overdraws it.

<a href="#">Link to this property</a>

has\_default\_payment\_method: boolean

Whether AI Gateway billing has a default payment method for the account.

<a href="#">Link to this property</a>

<details>

<summary>

payment\_method: object { brand, last4 }

The default payment method’s card. Null when there is no default, it isn’t a card, or it couldn’t be read.

</summary>

brand: optional string

Card brand, such as <code>visa</code>.

<a href="#">Link to this property</a>

last4: optional string

Last 4 digits of the card.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

topup\_config: object { amount, threshold, disabledReason, 2 more }

Auto top-up configuration, as GET /topup/config returns it.

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

<a href="#">Link to this property</a>

first\_topup\_success: optional boolean

Whether the account completed its first top-up. Auto top-up can be set up only after it.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result\_info: optional object { has\_more, page, per\_page, total\_count }

</summary>

has\_more: boolean

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20credit_balance%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get credit balance

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-gateway/billing/credit-balance \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "balance": 1250.5,
    "has_default_payment_method": true,
    "payment_method": {
      "brand": "visa",
      "last4": "4242"
    },
    "topup_config": {
      "amount": 5000,
      "threshold": 500,
      "disabledReason": "Payment failed after multiple retries",
      "error": "error",
      "lastFailedAt": 1700000000000
    },
    "first_topup_success": true
  },
  "success": true,
  "result_info": {
    "has_more": true,
    "page": 0,
    "per_page": 0,
    "total_count": 0
  }
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "balance": 1250.5,
    "has_default_payment_method": true,
    "payment_method": {
      "brand": "visa",
      "last4": "4242"
    },
    "topup_config": {
      "amount": 5000,
      "threshold": 500,
      "disabledReason": "Payment failed after multiple retries",
      "error": "error",
      "lastFailedAt": 1700000000000
    },
    "first_topup_success": true
  },
  "success": true,
  "result_info": {
    "has_more": true,
    "page": 0,
    "per_page": 0,
    "total_count": 0
  }
}
```