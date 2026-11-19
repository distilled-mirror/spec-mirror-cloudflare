---
title: Get top-up eligibility
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

# Get top-up eligibility

GET/accounts/{account\_id}/ai-gateway/billing/topup/eligibility

Reports whether the account can top up: its payment methods and whether each can pay for a top-up, whether a manual top-up is available and its limits, and the auto top-up state. Advisory only: every top-up checks again. Answers 409 while this endpoint isn’t available for the account yet.

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {auto\_topup, contract\_version, evaluated\_at, 4 more }

</summary>

<details>

<summary>

auto\_topup: object {can\_configure, config, limits, 3 more }

Auto top-up state.

</summary>

can\_configure: boolean

Whether auto top-up can be set up or changed now.

<a href="#">Link to this property</a>

<details>

<summary>

config: object {amount\_cents, threshold\_cents }

Configured threshold and amount. Null unless <code>state</code> is <code>active</code> or <code>needs_confirmation</code>.

</summary>

amount\_cents: number

Amount in cents that each auto top-up adds.

<a href="#">Link to this property</a>

threshold\_cents: number

Balance threshold in cents that triggers an auto top-up.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

limits: object {amount\_max\_cents, amount\_min\_cents, threshold\_min\_cents }

Allowed auto top-up values.

</summary>

amount\_max\_cents: number

Maximum auto top-up amount in cents.

<a href="#">Link to this property</a>

amount\_min\_cents: number

Minimum auto top-up amount in cents.

<a href="#">Link to this property</a>

threshold\_min\_cents: number

Minimum threshold in cents.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

payment\_method\_id: string

Payment method auto top-up charges or, once stopped, the one it stopped on. Null when there is none to name.

<a href="#">Link to this property</a>

<details>

<summary>

state: "first\_topup\_required"or "not\_configured"or "active"or 2 more

<code>first_topup_required</code>: auto top-up can be set up after the first manual top-up. <code>not_configured</code>: auto top-up is off. <code>active</code>: auto top-up is on. <code>needs_confirmation</code>: auto top-up is on, but its card has to be confirmed or replaced. <code>stopped</code>: auto top-up was turned off; <code>stopped_reason</code> says why, when known.

</summary>

One of the following:

"first\_topup\_required"

<a href="#">Link to this property</a>

"not\_configured"

<a href="#">Link to this property</a>

"active"

<a href="#">Link to this property</a>

"needs\_confirmation"

<a href="#">Link to this property</a>

"stopped"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

stopped\_reason: optional "payment\_method\_removed"or "payment\_method\_changed"or "expired\_card"or 4 more

Why auto top-up stopped. Present only when <code>state</code> is <code>stopped</code> and the reason is known.

</summary>

One of the following:

"payment\_method\_removed"

<a href="#">Link to this property</a>

"payment\_method\_changed"

<a href="#">Link to this property</a>

"expired\_card"

<a href="#">Link to this property</a>

"payment\_method\_not\_supported"

<a href="#">Link to this property</a>

"prepaid\_card\_not\_supported"

<a href="#">Link to this property</a>

"payment\_declined"

<a href="#">Link to this property</a>

"amount\_out\_of\_range"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

contract\_version: 2

Response contract version. Always <code>2</code>.

<a href="#">Link to this property</a>

evaluated\_at: string

When eligibility was evaluated, as an ISO 8601 timestamp.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

manual\_topup: object {available, default\_payment\_method\_id, limits }

Manual top-up availability.

</summary>

available: boolean

Whether a manual top-up can be made now. True only when <code>status</code> is <code>ready</code>.

<a href="#">Link to this property</a>

default\_payment\_method\_id: string

Payment method to preselect: the default when it can pay, otherwise the first that can. Null when none can.

<a href="#">Link to this property</a>

<details>

<summary>

limits: object {currency, max\_cents, min\_cents }

Allowed manual top-up amounts.

</summary>

currency: "USD"

Currency of the amounts. Always <code>USD</code>.

<a href="#">Link to this property</a>

max\_cents: number

Maximum top-up amount in cents.

<a href="#">Link to this property</a>

min\_cents: number

Minimum top-up amount in cents.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

payment\_methods: array of object {id, is\_default, type, 6 more }

The account’s payment methods, and whether each can pay for a top-up.

</summary>

id: string

Payment method identifier.

<a href="#">Link to this property</a>

is\_default: boolean

Whether this is the account’s default payment method.

<a href="#">Link to this property</a>

<details>

<summary>

type: "card"or "apple\_pay"or "google\_pay"or 3 more

Payment method type.

</summary>

One of the following:

"card"

<a href="#">Link to this property</a>

"apple\_pay"

<a href="#">Link to this property</a>

"google\_pay"

<a href="#">Link to this property</a>

"link"

<a href="#">Link to this property</a>

"paypal"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

usable: boolean

Whether this payment method can pay for a top-up.

<a href="#">Link to this property</a>

brand: optional string

Card brand. Present for cards.

<a href="#">Link to this property</a>

exp\_month: optional number

Expiration month, 1 to 12. Present for cards.

<a href="#">Link to this property</a>

exp\_year: optional number

Four-digit expiration year. Present for cards.

<a href="#">Link to this property</a>

last4: optional string

Last 4 digits. Present for cards.

<a href="#">Link to this property</a>

<details>

<summary>

unusable\_reason: optional "payment\_method\_not\_supported"or "expired\_card"or "prepaid\_card\_not\_supported"or "card\_not\_3ds\_capable"

Why this payment method can’t pay for a top-up. Present only when <code>usable</code> is false.

</summary>

One of the following:

"payment\_method\_not\_supported"

<a href="#">Link to this property</a>

"expired\_card"

<a href="#">Link to this property</a>

"prepaid\_card\_not\_supported"

<a href="#">Link to this property</a>

"card\_not\_3ds\_capable"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

reason: "NONE"or "CONTRACT\_BILLING"or "ACCOUNT\_RESTRICTED"or 3 more

What prevents a manual top-up, or <code>NONE</code>. <code>CONTRACT_BILLING</code>: the account is billed by contract. <code>ACCOUNT_RESTRICTED</code>: the account is restricted. <code>ELIGIBILITY_UNAVAILABLE</code>: eligibility could not be determined. <code>NO_ELIGIBLE_PAYMENT_METHOD</code>: no payment method can pay for a top-up. <code>DAILY_LIMIT_REACHED</code>: the account reached its daily top-up limit.

</summary>

One of the following:

"NONE"

<a href="#">Link to this property</a>

"CONTRACT\_BILLING"

<a href="#">Link to this property</a>

"ACCOUNT\_RESTRICTED"

<a href="#">Link to this property</a>

"ELIGIBILITY\_UNAVAILABLE"

<a href="#">Link to this property</a>

"NO\_ELIGIBLE\_PAYMENT\_METHOD"

<a href="#">Link to this property</a>

"DAILY\_LIMIT\_REACHED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

status: "ready"or "blocked"or "unavailable"

<code>ready</code> when a manual top-up is available, <code>blocked</code> when <code>reason</code> prevents one, or <code>unavailable</code> when eligibility could not be determined and the request can be retried.

</summary>

One of the following:

"ready"

<a href="#">Link to this property</a>

"blocked"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(method)%20get_eligibility%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get top-up eligibility

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-gateway/billing/topup/eligibility \
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
    "auto_topup": {
      "can_configure": true,
      "config": {
        "amount_cents": 5000,
        "threshold_cents": 500
      },
      "limits": {
        "amount_max_cents": 100000,
        "amount_min_cents": 1000,
        "threshold_min_cents": 500
      },
      "payment_method_id": "pm_123",
      "state": "active",
      "stopped_reason": "payment_declined"
    },
    "contract_version": 2,
    "evaluated_at": "2026-11-18T12:00:00Z",
    "manual_topup": {
      "available": true,
      "default_payment_method_id": "pm_123",
      "limits": {
        "currency": "USD",
        "max_cents": 100000,
        "min_cents": 1000
      }
    },
    "payment_methods": [
      {
        "id": "pm_123",
        "is_default": true,
        "type": "card",
        "usable": true,
        "brand": "visa",
        "exp_month": 12,
        "exp_year": 2030,
        "last4": "4242",
        "unusable_reason": "expired_card"
      }
    ],
    "reason": "NONE",
    "status": "ready"
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
    "auto_topup": {
      "can_configure": true,
      "config": {
        "amount_cents": 5000,
        "threshold_cents": 500
      },
      "limits": {
        "amount_max_cents": 100000,
        "amount_min_cents": 1000,
        "threshold_min_cents": 500
      },
      "payment_method_id": "pm_123",
      "state": "active",
      "stopped_reason": "payment_declined"
    },
    "contract_version": 2,
    "evaluated_at": "2026-11-18T12:00:00Z",
    "manual_topup": {
      "available": true,
      "default_payment_method_id": "pm_123",
      "limits": {
        "currency": "USD",
        "max_cents": 100000,
        "min_cents": 1000
      }
    },
    "payment_methods": [
      {
        "id": "pm_123",
        "is_default": true,
        "type": "card",
        "usable": true,
        "brand": "visa",
        "exp_month": 12,
        "exp_year": 2030,
        "last4": "4242",
        "unusable_reason": "expired_card"
      }
    ],
    "reason": "NONE",
    "status": "ready"
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