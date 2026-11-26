---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Get invoice preview
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Get invoice preview

GET/accounts/{account\_id}/ai-gateway/billing/invoice-preview

Retrieve a preview of the upcoming invoice including line items and tax.

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

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

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

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { id, amount\_due, amount\_paid, 6 more }

</summary>

id: string

Invoice number, as printed on the invoice, rather than an identifier. Empty until the invoice is finalized.

<a href="#">Link to this property</a>

amount\_due: number

Amount due, in US cents.

<a href="#">Link to this property</a>

amount\_paid: number

Amount paid, in US cents.

<a href="#">Link to this property</a>

amount\_remaining: number

Amount still owed, in US cents.

<a href="#">Link to this property</a>

currency: string

Lowercase ISO 4217 currency code.

<a href="#">Link to this property</a>

<details>

<summary>

invoice\_lines: array of object { amount, currency, description, 4 more }

Invoice line items.

</summary>

amount: number

Line item amount, in US cents.

<a href="#">Link to this property</a>

currency: string

Lowercase ISO 4217 currency code.

<a href="#">Link to this property</a>

description: string

Line item description.

<a href="#">Link to this property</a>

<details>

<summary>

period: object { end, start }

Period the line item covers.

</summary>

end: number

End of the period, as a Unix timestamp in seconds.

<a href="#">Link to this property</a>

start: number

Start of the period, as a Unix timestamp in seconds.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

pricing: object { unit\_amount\_decimal }

Line item pricing.

</summary>

unit\_amount\_decimal: string

Unit price in US cents, as a decimal string.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

quantity: number

Quantity billed.

<a href="#">Link to this property</a>

<details>

<summary>

pretax\_credit\_amounts: optional array of object { amount, type, credit\_balance\_transaction, discount }

Credits applied to the line item before tax.

</summary>

amount: number

Credit applied, in US cents.

<a href="#">Link to this property</a>

type: string

Credit type: <code>credit_balance_transaction</code> or <code>discount</code>.

<a href="#">Link to this property</a>

credit\_balance\_transaction: optional string

Credit balance transaction identifier, when <code>type</code> is <code>credit_balance_transaction</code>.

<a href="#">Link to this property</a>

discount: optional string

Discount identifier, when <code>type</code> is <code>discount</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

period\_end: number

End of the billing period, as a Unix timestamp in seconds.

<a href="#">Link to this property</a>

period\_start: number

Start of the billing period, as a Unix timestamp in seconds.

<a href="#">Link to this property</a>

<details>

<summary>

status: "draft" or "open" or "paid" or 2 more

Invoice status.

</summary>

One of the following:

"draft"

<a href="#">Link to this property</a>

"open"

<a href="#">Link to this property</a>

"paid"

<a href="#">Link to this property</a>

"uncollectible"

<a href="#">Link to this property</a>

"void"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

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

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_preview%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get invoice preview

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-gateway/billing/invoice-preview \
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
    "id": "id",
    "amount_due": 1250,
    "amount_paid": 0,
    "amount_remaining": 1250,
    "currency": "usd",
    "invoice_lines": [
      {
        "amount": 1250,
        "currency": "usd",
        "description": "description",
        "period": {
          "end": 1702592000,
          "start": 1700000000
        },
        "pricing": {
          "unit_amount_decimal": "unit_amount_decimal"
        },
        "quantity": 0,
        "pretax_credit_amounts": [
          {
            "amount": 500,
            "type": "credit_balance_transaction",
            "credit_balance_transaction": "credit_balance_transaction",
            "discount": "discount"
          }
        ]
      }
    ],
    "period_end": 1702592000,
    "period_start": 1700000000,
    "status": "draft"
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
    "id": "id",
    "amount_due": 1250,
    "amount_paid": 0,
    "amount_remaining": 1250,
    "currency": "usd",
    "invoice_lines": [
      {
        "amount": 1250,
        "currency": "usd",
        "description": "description",
        "period": {
          "end": 1702592000,
          "start": 1700000000
        },
        "pricing": {
          "unit_amount_decimal": "unit_amount_decimal"
        },
        "quantity": 0,
        "pretax_credit_amounts": [
          {
            "amount": 500,
            "type": "credit_balance_transaction",
            "credit_balance_transaction": "credit_balance_transaction",
            "discount": "discount"
          }
        ]
      }
    ],
    "period_end": 1702592000,
    "period_start": 1700000000,
    "status": "draft"
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