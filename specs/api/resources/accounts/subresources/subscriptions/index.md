---
title: Subscriptions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Accounts](https://developers.cloudflare.com/api/resources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Subscriptions

##### [List Subscriptions](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/subscriptions

##### [Get Subscription](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/get_by_identifier)

GET/accounts/{account\_id}/subscriptions/{subscription\_identifier}

##### [Create Subscription](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/subscriptions

##### [Update Subscription](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/update)

PUT/accounts/{account\_id}/subscriptions/{subscription\_identifier}

##### [Delete Subscription](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/delete)

DELETE/accounts/{account\_id}/subscriptions/{subscription\_identifier}

##### [Cancel Delayed Downgrade](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/methods/cancel_downgrade)

POST/accounts/{account\_id}/subscriptions/cancel-downgrade

##### ModelsExpand Collapse

<details>

<summary>

SubscriptionDeleteResponse object {subscription\_id }

</summary>

subscription\_id: optional string

Subscription identifier tag.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.subscriptions%20%3E%20(model)%20subscription_delete_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionCancelDowngradeResponse = unknownor string

</summary>

One of the following:

unknown

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.subscriptions%20%3E%20(model)%20subscription_cancel_downgrade_response%20%3E%20(schema)>)

#### SubscriptionsCancel Reason

##### [Create Cancel Reason](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/subresources/cancel_reason/methods/create)

POST/accounts/{account\_id}/subscriptions/{subscription\_identifier}/cancel-reason

##### [Get Cancel Reason](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/subresources/cancel_reason/methods/get)

GET/accounts/{account\_id}/subscriptions/{subscription\_identifier}/cancel-reason

##### ModelsExpand Collapse

<details>

<summary>

CancelReasonCreateResponse object {id, other, reason\_code, 2 more }

</summary>

id: optional string

The cancel reason identifier.

<a href="#">Link to this property</a>

other: optional string

Additional cancellation details.

<a href="#">Link to this property</a>

reason\_code: optional array of string

The cancellation reason codes.

<a href="#">Link to this property</a>

submitted: optional string

When the cancel reason was submitted.

formatdate-time

<a href="#">Link to this property</a>

subscription\_id: optional string

The subscription identifier.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.subscriptions.cancel_reason%20%3E%20(model)%20cancel_reason_create_response%20%3E%20(schema)>)

<details>

<summary>

CancelReasonGetResponse object {id, other, reason\_code, 2 more }

</summary>

id: optional string

The cancel reason identifier.

<a href="#">Link to this property</a>

other: optional string

Additional cancellation details.

<a href="#">Link to this property</a>

reason\_code: optional array of string

The cancellation reason codes.

<a href="#">Link to this property</a>

submitted: optional string

When the cancel reason was submitted.

formatdate-time

<a href="#">Link to this property</a>

subscription\_id: optional string

The subscription identifier.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.subscriptions.cancel_reason%20%3E%20(model)%20cancel_reason_get_response%20%3E%20(schema)>)

#### SubscriptionsActions

##### [Append Subscription Action](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/subresources/actions/methods/append)

POST/accounts/{account\_id}/subscriptions/{subscription\_identifier}/action/append

#### SubscriptionsBulk

##### [Create Subscriptions](https://developers.cloudflare.com/api/resources/accounts/subresources/subscriptions/subresources/bulk/methods/create)

POST/accounts/{account\_id}/bulk/subscriptions

##### ModelsExpand Collapse

<details>

<summary>

BulkCreateResponse object {client\_secrets, subscriptions }

</summary>

client\_secrets: optional array of string

<a href="#">Link to this property</a>

<details>

<summary>

subscriptions: optional array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20subscription%20%3E%20(schema)">Subscription</a> { id, currency, current\_period\_end, 5 more }

</summary>

id: optional string

Subscription identifier tag.

maxLength32

<a href="#">Link to this property</a>

currency: optional string

The monetary unit in which pricing information is displayed.

<a href="#">Link to this property</a>

current\_period\_end: optional string

The end of the current period and also when the next billing is due.

formatdate-time

<a href="#">Link to this property</a>

current\_period\_start: optional string

When the current billing period started. May match initial\_period\_start if this is the first period.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

frequency: optional "weekly"or "monthly"or "quarterly"or "yearly"

How often the subscription is renewed automatically.

</summary>

One of the following:

"weekly"

<a href="#">Link to this property</a>

"monthly"

<a href="#">Link to this property</a>

"quarterly"

<a href="#">Link to this property</a>

"yearly"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

price: optional number

The price of the subscription that will be billed, in US dollars.

<a href="#">Link to this property</a>

rate\_plan: optional <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20rate_plan%20%3E%20(schema)">RatePlan</a> { id, currency, externally\_managed, 4 more }

The rate plan applied to the subscription.

<a href="#">Link to this property</a>

<details>

<summary>

state: optional "Trial"or "Provisioned"or "Paid"or 4 more

The state that the subscription is in.

</summary>

One of the following:

"Trial"

<a href="#">Link to this property</a>

"Provisioned"

<a href="#">Link to this property</a>

"Paid"

<a href="#">Link to this property</a>

"AwaitingPayment"

<a href="#">Link to this property</a>

"Cancelled"

<a href="#">Link to this property</a>

"Failed"

<a href="#">Link to this property</a>

"Expired"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.subscriptions.bulk%20%3E%20(model)%20bulk_create_response%20%3E%20(schema)>)