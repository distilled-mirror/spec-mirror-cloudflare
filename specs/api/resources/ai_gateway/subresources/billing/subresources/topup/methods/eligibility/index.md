---
title: Check top-up eligibility (deprecated)
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

[Topup](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Check top-up eligibility (deprecated)

Deprecated

POST/accounts/{account\_id}/ai-gateway/billing/topup/eligibility

Deprecated: use GET /topup/eligibility, which reads the account’s payment methods itself. This endpoint keeps working while that one answers 409 for the account. Reports whether the account can make a manual top-up, given the payment methods in the request body. Advisory only: every top-up checks again.

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

`Billing Write``Billing Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

contract\_version: optional number

Not accepted: any value answers 400. Read the current eligibility with GET /topup/eligibility.

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(params)%200%20%3E%20(param)%20contract_version%20%3E%20(schema)>)

<details>

<summary>

payment\_methods: optional array of object { default, last\_four, type }

The account’s payment methods. Omit it, or send an empty list, when there are none.

</summary>

default: optional boolean

Whether this is the account default payment method.

<a href="#">Link to this property</a>

last\_four: optional string

Last 4 digits, for display copy only.

<a href="#">Link to this property</a>

type: optional string

Payment-method type. Absent or unrecognized is treated as non-card (does not error). Known values: PAYPAL, CREDIT\_CARD, APPLE\_PAY, GOOGLE\_PAY, ACH\_DIRECT\_DEBIT, SEPA\_DEBIT, CASHAPP, LINK, CRYPTO.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(params)%200%20%3E%20(param)%20payment_methods%20%3E%20(schema)>)

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { account\_payment\_method\_state, aig\_customer\_state, aig\_default\_payment\_method\_state, 5 more }

</summary>

<details>

<summary>

account\_payment\_method\_state: "NONE" or "UNSUPPORTED\_ONLY" or "SUPPORTED\_PRESENT" or "UNKNOWN"

Account-level payment-method state derived from the provided list.

</summary>

One of the following:

"NONE"

<a href="#">Link to this property</a>

"UNSUPPORTED\_ONLY"

<a href="#">Link to this property</a>

"SUPPORTED\_PRESENT"

<a href="#">Link to this property</a>

"UNKNOWN"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

aig\_customer\_state: "RESOLVED" or "RESOLUTION\_FAILED"

AI Gateway billing profile resolution outcome.

</summary>

One of the following:

"RESOLVED"

<a href="#">Link to this property</a>

"RESOLUTION\_FAILED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

aig\_default\_payment\_method\_state: "PRESENT" or "MISSING"

Whether AI Gateway billing has a default payment method.

</summary>

One of the following:

"PRESENT"

<a href="#">Link to this property</a>

"MISSING"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

display\_payment\_method: object { last4, brand }

Card to reference in the UI, e.g. “use card ending 1234”.

</summary>

last4: string

Last 4 digits of the card.

<a href="#">Link to this property</a>

brand: optional string

Card brand, when known.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

eligible: boolean

True only when reason === ELIGIBLE.

<a href="#">Link to this property</a>

<details>

<summary>

reason: "ELIGIBLE" or "NO\_ACCOUNT\_PAYMENT\_METHOD" or "UNSUPPORTED\_ACCOUNT\_PAYMENT\_METHOD" or 6 more

Canonical eligibility outcome for display and support triage.

</summary>

One of the following:

"ELIGIBLE"

<a href="#">Link to this property</a>

"NO\_ACCOUNT\_PAYMENT\_METHOD"

<a href="#">Link to this property</a>

"UNSUPPORTED\_ACCOUNT\_PAYMENT\_METHOD"

<a href="#">Link to this property</a>

"ACCOUNT\_PAYMENT\_METHOD\_NOT\_DEFAULT"

<a href="#">Link to this property</a>

"ACCOUNT\_PAYMENT\_METHOD\_NOT\_LINKED\_TO\_AIG"

<a href="#">Link to this property</a>

"CONTRACT\_BILLING\_NOT\_SELF\_SERVE"

<a href="#">Link to this property</a>

"AIG\_CUSTOMER\_RESOLUTION\_FAILED"

<a href="#">Link to this property</a>

"PENDING\_3DS\_AUTHENTICATION"

<a href="#">Link to this property</a>

"PAYMENT\_AUTHENTICATION\_FAILED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recommended\_action: "NONE" or "ADD\_SUPPORTED\_PAYMENT\_METHOD" or "USE\_EXISTING\_CARD" or 4 more

Machine-readable next step.

</summary>

One of the following:

"NONE"

<a href="#">Link to this property</a>

"ADD\_SUPPORTED\_PAYMENT\_METHOD"

<a href="#">Link to this property</a>

"USE\_EXISTING\_CARD"

<a href="#">Link to this property</a>

"SET\_CARD\_AS\_DEFAULT"

<a href="#">Link to this property</a>

"CONTACT\_SUPPORT"

<a href="#">Link to this property</a>

"RESUME\_AUTHENTICATION"

<a href="#">Link to this property</a>

"RETRY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

recoverable: boolean

Whether the customer can resolve this themselves (vs contact support).

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Check top-up eligibility (deprecated)

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-gateway/billing/topup/eligibility \
    -X POST \
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
    "account_payment_method_state": "SUPPORTED_PRESENT",
    "aig_customer_state": "RESOLVED",
    "aig_default_payment_method_state": "MISSING",
    "display_payment_method": {
      "last4": "1234",
      "brand": "visa"
    },
    "eligible": false,
    "reason": "ACCOUNT_PAYMENT_METHOD_NOT_LINKED_TO_AIG",
    "recommended_action": "USE_EXISTING_CARD",
    "recoverable": true
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
    "account_payment_method_state": "SUPPORTED_PRESENT",
    "aig_customer_state": "RESOLVED",
    "aig_default_payment_method_state": "MISSING",
    "display_payment_method": {
      "last4": "1234",
      "brand": "visa"
    },
    "eligible": false,
    "reason": "ACCOUNT_PAYMENT_METHOD_NOT_LINKED_TO_AIG",
    "recommended_action": "USE_EXISTING_CARD",
    "recoverable": true
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