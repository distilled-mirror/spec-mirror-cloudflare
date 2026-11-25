---
agent:
  instructions: "This site offers a search API that returns relevant content across the entire site. Use the search endpoint to find information instead of crawling individual pages."
  search: "https://developers.cloudflare.com/.well-known/search?q={query}"
title: Topup
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

[Billing](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Topup

##### [Create a top-up](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/methods/create)

POST/accounts/{account\_id}/ai-gateway/billing/topup

##### [Check top-up status](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/methods/status)

POST/accounts/{account\_id}/ai-gateway/billing/topup/status

##### [Check top-up eligibility (deprecated)](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/methods/eligibility)

Deprecated

POST/accounts/{account\_id}/ai-gateway/billing/topup/eligibility

##### [Get top-up eligibility](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/methods/get_eligibility)

GET/accounts/{account\_id}/ai-gateway/billing/topup/eligibility

##### [Get account top-up limits (deprecated)](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/billing/subresources/topup/methods/limits)

Deprecated

GET/accounts/{account\_id}/ai-gateway/billing/topup/limits

##### ModelsExpand Collapse

<details>

<summary>

TopupCreateResponse object { client\_secret, onboarding, payment\_intent\_id, 2 more }

</summary>

client\_secret: string

Client secret used to complete payment authentication.

<a href="#">Link to this property</a>

onboarding: boolean

Whether the user was already onboarded.

<a href="#">Link to this property</a>

payment\_intent\_id: string

Top-up payment identifier.

<a href="#">Link to this property</a>

brand: optional string

Card brand (visa, mastercard, etc.).

<a href="#">Link to this property</a>

last4: optional string

Last 4 digits of card.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(model)%20topup_create_response%20%3E%20(schema)>)

<details>

<summary>

TopupStatusResponse object { payment\_intent\_id, status }

</summary>

payment\_intent\_id: string

Top-up identifier from the request.

<a href="#">Link to this property</a>

<details>

<summary>

status: "completed" or "pending"

<code>completed</code> once the top-up payment is processed and its credits are added to the balance, <code>pending</code> until then.

</summary>

One of the following:

"completed"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(model)%20topup_status_response%20%3E%20(schema)>)

<details>

<summary>

TopupEligibilityResponse object { account\_payment\_method\_state, aig\_customer\_state, aig\_default\_payment\_method\_state, 5 more }

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(model)%20topup_eligibility_response%20%3E%20(schema)>)

<details>

<summary>

TopupGetEligibilityResponse object { auto\_topup, contract\_version, evaluated\_at, 4 more }

</summary>

<details>

<summary>

auto\_topup: object { can\_configure, config, limits, 3 more }

Auto top-up state.

</summary>

can\_configure: boolean

Whether auto top-up can be set up or changed now.

<a href="#">Link to this property</a>

<details>

<summary>

config: object { amount\_cents, threshold\_cents }

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

limits: object { amount\_max\_cents, amount\_min\_cents, threshold\_min\_cents }

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

state: "first\_topup\_required" or "not\_configured" or "active" or 2 more

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

stopped\_reason: optional "payment\_method\_removed" or "payment\_method\_changed" or "expired\_card" or 4 more

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

manual\_topup: object { available, default\_payment\_method\_id, limits }

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

limits: object { currency, max\_cents, min\_cents }

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

payment\_methods: array of object { id, is\_default, type, 6 more }

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

type: "card" or "apple\_pay" or "google\_pay" or 3 more

Payment method type. A card saved in a wallet has the wallet type and its card details. <code>link</code> is a card saved with Link, which has card details, or a Link payment that no card funds, which has none.

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

Card brand. Present for cards, including cards saved in a wallet.

<a href="#">Link to this property</a>

exp\_month: optional number

Expiration month, 1 to 12. Present for cards, including cards saved in a wallet.

<a href="#">Link to this property</a>

exp\_year: optional number

Four-digit expiration year. Present for cards, including cards saved in a wallet.

<a href="#">Link to this property</a>

last4: optional string

Last 4 digits. Present for cards, including cards saved in a wallet.

<a href="#">Link to this property</a>

<details>

<summary>

unusable\_reason: optional "payment\_method\_not\_supported" or "expired\_card" or "prepaid\_card\_not\_supported" or "card\_not\_3ds\_capable"

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

reason: "NONE" or "CONTRACT\_BILLING" or "ACCOUNT\_RESTRICTED" or 3 more

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

status: "ready" or "blocked" or "unavailable"

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

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(model)%20topup_get_eligibility_response%20%3E%20(schema)>)

<details>

<summary>

TopupLimitsResponse object { currency, max\_cents, min\_cents }

</summary>

currency: string

ISO 4217 currency code.

<a href="#">Link to this property</a>

max\_cents: number

Maximum allowed top-up amount in cents.

<a href="#">Link to this property</a>

min\_cents: number

Minimum allowed top-up amount in cents.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.billing.topup%20%3E%20(model)%20topup_limits_response%20%3E%20(schema)>)

#### TopupConfig

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