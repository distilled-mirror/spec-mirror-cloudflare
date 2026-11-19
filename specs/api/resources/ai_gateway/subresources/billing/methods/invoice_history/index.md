---
title: Get invoice history
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get invoice history

GET/accounts/{account\_id}/ai-gateway/billing/invoice-history

Retrieve a list of past invoices with pagination, optionally filtered by type.

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

`AI Gateway Write``AI Gateway Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

type: optional "auto"or "all"or "manual"

Filter invoice type: auto, manual, or all.

</summary>

One of the following:

"auto"

<a href="#">Link to this property</a>

"all"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(params)%20default%20%3E%20(param)%20type%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {invoices, pagination }

</summary>

<details>

<summary>

invoices: array of object {amount\_due, amount\_paid, amount\_remaining, 11 more }

Top-up invoices matching <code>type</code>, up to 100.

</summary>

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

id: optional string

Invoice number, as printed on the invoice, rather than an identifier. Null until the invoice is finalized.

<a href="#">Link to this property</a>

attempt\_count: optional number

Number of payment attempts.

<a href="#">Link to this property</a>

attempted: optional boolean

Whether payment was attempted.

<a href="#">Link to this property</a>

auto\_advance: optional boolean

Whether the invoice is finalized and collected without an explicit action. False for top-up invoices, which are charged when the top-up is made.

<a href="#">Link to this property</a>

created: optional number

When the invoice was created, as a Unix timestamp in seconds.

<a href="#">Link to this property</a>

created\_by: optional string

What created the invoice. Always <code>AI_GATEWAY</code>.

<a href="#">Link to this property</a>

description: optional string

Invoice description.

<a href="#">Link to this property</a>

invoice\_origin: optional string

How the top-up was made: <code>auto</code> or <code>manual</code>.

<a href="#">Link to this property</a>

invoice\_pdf: optional string

URL of the invoice PDF. Null until the invoice is finalized.

<a href="#">Link to this property</a>

status: optional string

Invoice status: <code>draft</code>, <code>open</code>, <code>paid</code>, <code>uncollectible</code>, or <code>void</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

pagination: object {has\_more, page, per\_page, total\_count }

Pagination details. Results come in a single page.

</summary>

has\_more: boolean

Whether more invoices match than returned.

<a href="#">Link to this property</a>

page: number

Page number. Always 1.

<a href="#">Link to this property</a>

per\_page: number

Page size.

<a href="#">Link to this property</a>

total\_count: number

Number of matching invoices.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result\_info: optional object {has\_more, page, per\_page, total\_count }

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

[Link to this property](#)%20ai_gateway.billing%20%3E%20(method)%20invoice_history%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get invoice history

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-gateway/billing/invoice-history \
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
    "invoices": [
      {
        "amount_due": 5000,
        "amount_paid": 5000,
        "amount_remaining": 0,
        "currency": "usd",
        "id": "id",
        "attempt_count": 0,
        "attempted": true,
        "auto_advance": true,
        "created": 1700000000,
        "created_by": "created_by",
        "description": "description",
        "invoice_origin": "manual",
        "invoice_pdf": "invoice_pdf",
        "status": "paid"
      }
    ],
    "pagination": {
      "has_more": true,
      "page": 0,
      "per_page": 0,
      "total_count": 0
    }
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
    "invoices": [
      {
        "amount_due": 5000,
        "amount_paid": 5000,
        "amount_remaining": 0,
        "currency": "usd",
        "id": "id",
        "attempt_count": 0,
        "attempted": true,
        "auto_advance": true,
        "created": 1700000000,
        "created_by": "created_by",
        "description": "description",
        "invoice_origin": "manual",
        "invoice_pdf": "invoice_pdf",
        "status": "paid"
      }
    ],
    "pagination": {
      "has_more": true,
      "page": 0,
      "per_page": 0,
      "total_count": 0
    }
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