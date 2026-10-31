---
title: Activity
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Billing](https://developers.cloudflare.com/api/resources/billing)

[Spend Policies](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Activity

##### [List Spend Policy Activity](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies/subresources/activity/methods/list)

GET/accounts/{account\_id}/billing/spend-policies/activity

##### ModelsExpand Collapse

<details>

<summary>

ActivityListResponse object {id, action, actor, 5 more }

</summary>

id: string

<a href="#">Link to this property</a>

<details>

<summary>

action: "created"or "updated"or "enabled"or 2 more

</summary>

One of the following:

"created"

<a href="#">Link to this property</a>

"updated"

<a href="#">Link to this property</a>

"enabled"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

"deleted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

actor: string

Verified actor identifier, unknown when absent, or trusted internal actor.

<a href="#">Link to this property</a>

<details>

<summary>

details: object {after, before }

</summary>

<details>

<summary>

after: optional object {id, account\_id, action, 7 more }

A spend policy.

</summary>

id: string

The unique identifier of the spend policy.

formatuuid

<a href="#">Link to this property</a>

account\_id: number

Internal numeric ID of the account that owns the policy. This is not the account tag used in the path.

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

action: "notification"or "usage\_block"

The action taken when the threshold is reached. <code>notification</code> sends an email to <code>notification_email</code>. <code>usage_block</code> blocks further usage of the product until the end of the billing period. Raising the threshold above the current balance, disabling the policy, or deleting it lifts the block early.

</summary>

One of the following:

"notification"

<a href="#">Link to this property</a>

"usage\_block"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is evaluated.

<a href="#">Link to this property</a>

name: string

Display name of the policy.

<a href="#">Link to this property</a>

notification\_email: string

Email address that receives notifications. An empty string when none is set.

<a href="#">Link to this property</a>

<details>

<summary>

product\_id: "workers"or "durable\_objects"

The product the policy applies to: <code>workers</code> or <code>durable_objects</code>. Each product’s balance and policies are separate. Both products support <code>notification</code> and <code>usage_block</code> policies on create and update.

</summary>

One of the following:

"workers"

<a href="#">Link to this property</a>

"durable\_objects"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

threshold\_cents: number

The spend threshold for the current billing period, in US cents.

formatint64

<a href="#">Link to this property</a>

version: number

Optimistic-concurrency version. It starts at 1 and goes up by one on every update or delete. This value is also returned in <code>ETag</code>.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

current\_state: optional object {balance\_cents, billing\_period\_end, billing\_period\_start, 3 more }

Read-only state on list/get responses, evaluated from the latest owning projector snapshot at request time, independently of the API replica. Configuration enabled/version/ETag do not change when a cycle rolls over. Audit history remains unchanged. Missing during a rolling upgrade or on mutation responses; clients must treat missing state as unavailable. Balances are asynchronous estimates, not a synchronous usage read.

</summary>

balance\_cents: number

formatint64

<a href="#">Link to this property</a>

billing\_period\_end: string

formatdate-time

<a href="#">Link to this property</a>

billing\_period\_start: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

enforcement: object {applied\_generation, delivery\_status, desired\_generation, 2 more }

Durable desired cap and delivery bookkeeping for this policy, or null if no owned effect exists. Separate from threshold evaluation: pending/leased/retry can lag the new billing period. Succeeded with equal generations means delivery completed, not an EWC readback.

</summary>

applied\_generation: number

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

delivery\_status: "pending"or "leased"or "retry"or "succeeded"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"leased"

<a href="#">Link to this property</a>

"retry"

<a href="#">Link to this property</a>

"succeeded"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

desired\_generation: number

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

desired\_state: "active"or "inactive"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

expires\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

evaluated\_at: string

Evaluation time; not the timestamp of the latest usage event.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "disabled"or "no\_current\_period"or "unavailable"or 3 more

Threshold evaluation, not proof of an edge cap. No current active period yields no\_current\_period for enabled policies; failed aggregate reads yield unavailable for enabled policies. Disabled policies report disabled. Neither no\_current\_period nor unavailable implies a zero balance or below-limit state. Operators may disable current-state reads, in which case current\_state is omitted.

</summary>

One of the following:

"disabled"

<a href="#">Link to this property</a>

"no\_current\_period"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

"below\_limit"

<a href="#">Link to this property</a>

"approaching\_limit"

<a href="#">Link to this property</a>

"limit\_reached"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

before: optional object {id, account\_id, action, 7 more }

Prior configuration; null on creation or if a previous revision is unavailable.

</summary>

id: string

The unique identifier of the spend policy.

formatuuid

<a href="#">Link to this property</a>

account\_id: number

Internal numeric ID of the account that owns the policy. This is not the account tag used in the path.

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

action: "notification"or "usage\_block"

The action taken when the threshold is reached. <code>notification</code> sends an email to <code>notification_email</code>. <code>usage_block</code> blocks further usage of the product until the end of the billing period. Raising the threshold above the current balance, disabling the policy, or deleting it lifts the block early.

</summary>

One of the following:

"notification"

<a href="#">Link to this property</a>

"usage\_block"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is evaluated.

<a href="#">Link to this property</a>

name: string

Display name of the policy.

<a href="#">Link to this property</a>

notification\_email: string

Email address that receives notifications. An empty string when none is set.

<a href="#">Link to this property</a>

<details>

<summary>

product\_id: "workers"or "durable\_objects"

The product the policy applies to: <code>workers</code> or <code>durable_objects</code>. Each product’s balance and policies are separate. Both products support <code>notification</code> and <code>usage_block</code> policies on create and update.

</summary>

One of the following:

"workers"

<a href="#">Link to this property</a>

"durable\_objects"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

threshold\_cents: number

The spend threshold for the current billing period, in US cents.

formatint64

<a href="#">Link to this property</a>

version: number

Optimistic-concurrency version. It starts at 1 and goes up by one on every update or delete. This value is also returned in <code>ETag</code>.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

current\_state: optional object {balance\_cents, billing\_period\_end, billing\_period\_start, 3 more }

Read-only state on list/get responses, evaluated from the latest owning projector snapshot at request time, independently of the API replica. Configuration enabled/version/ETag do not change when a cycle rolls over. Audit history remains unchanged. Missing during a rolling upgrade or on mutation responses; clients must treat missing state as unavailable. Balances are asynchronous estimates, not a synchronous usage read.

</summary>

balance\_cents: number

formatint64

<a href="#">Link to this property</a>

billing\_period\_end: string

formatdate-time

<a href="#">Link to this property</a>

billing\_period\_start: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

enforcement: object {applied\_generation, delivery\_status, desired\_generation, 2 more }

Durable desired cap and delivery bookkeeping for this policy, or null if no owned effect exists. Separate from threshold evaluation: pending/leased/retry can lag the new billing period. Succeeded with equal generations means delivery completed, not an EWC readback.

</summary>

applied\_generation: number

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

delivery\_status: "pending"or "leased"or "retry"or "succeeded"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"leased"

<a href="#">Link to this property</a>

"retry"

<a href="#">Link to this property</a>

"succeeded"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

desired\_generation: number

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

desired\_state: "active"or "inactive"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

expires\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

evaluated\_at: string

Evaluation time; not the timestamp of the latest usage event.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "disabled"or "no\_current\_period"or "unavailable"or 3 more

Threshold evaluation, not proof of an edge cap. No current active period yields no\_current\_period for enabled policies; failed aggregate reads yield unavailable for enabled policies. Disabled policies report disabled. Neither no\_current\_period nor unavailable implies a zero balance or below-limit state. Operators may disable current-state reads, in which case current\_state is omitted.

</summary>

One of the following:

"disabled"

<a href="#">Link to this property</a>

"no\_current\_period"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

"below\_limit"

<a href="#">Link to this property</a>

"approaching\_limit"

<a href="#">Link to this property</a>

"limit\_reached"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

occurred\_at: string

formatdate-time

<a href="#">Link to this property</a>

policy\_id: string

The unique identifier of the spend policy.

formatuuid

<a href="#">Link to this property</a>

policy\_version: number

formatint64

minimum1

<a href="#">Link to this property</a>

product\_id: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(model)%20activity_list_response%20%3E%20(schema)>)