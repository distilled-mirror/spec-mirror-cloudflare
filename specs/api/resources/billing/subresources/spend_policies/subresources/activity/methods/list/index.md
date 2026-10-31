---
title: List Spend Policy Activity
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Billing](https://developers.cloudflare.com/api/resources/billing)

[Spend Policies](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies)

[Activity](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies/subresources/activity)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Spend Policy Activity

GET/accounts/{account\_id}/billing/spend-policies/activity

Returns configuration history from immutable policy revisions for the account, including deleted policies. Entries contain before/after values and verified actor attribution. Pages use descending revision IDs, not event or commit order; refresh the first page for new entries. This cursor is not an incremental consumer checkpoint.

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

##### P ath ParametersExpand Collapse

account\_id: string

Represents a Cloudflare resource identifier tag.

maxLength32

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Opaque token from the preceding response’s result\_info.cursor. Pass it unchanged to retrieve older entries.

maxLength1024

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

limit: optional number

Maximum number of audit entries to return. Defaults to 50. Values above 100 are capped at 100 rather than rejected.

minimum1

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message, code }

Always empty on success.

</summary>

message: string

Describes the error or notice.

<a href="#">Link to this property</a>

code: optional number

Identifies the error or notice type.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

Contains informational notices about the response.

</summary>

message: string

Describes the error or notice.

<a href="#">Link to this property</a>

code: optional number

Identifies the error or notice type.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, action, actor, 5 more }

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

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, cursor }

</summary>

count: number

Number of entries in this response.

minimum0

<a href="#">Link to this property</a>

cursor: optional string

Opaque next-page token. Omitted when no older entries were visible at query time.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

Indicates whether the API call was successful.

[Link to this property](#)%20billing.spend_policies.activity%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Spend Policy Activity

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/billing/spend-policies/activity \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "message": "message",
      "code": 0
    }
  ],
  "messages": [
    {
      "message": "message",
      "code": 0
    }
  ],
  "result": [
    {
      "id": "id",
      "action": "created",
      "actor": "actor",
      "details": {
        "after": {
          "id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
          "account_id": 1234567,
          "action": "notification",
          "enabled": true,
          "name": "Workers cap",
          "notification_email": "billing@example.com",
          "product_id": "workers",
          "threshold_cents": 100,
          "version": 1,
          "current_state": {
            "balance_cents": 0,
            "billing_period_end": "2019-12-27T18:11:19.117Z",
            "billing_period_start": "2019-12-27T18:11:19.117Z",
            "enforcement": {
              "applied_generation": 0,
              "delivery_status": "pending",
              "desired_generation": 0,
              "desired_state": "active",
              "expires_at": "2019-12-27T18:11:19.117Z"
            },
            "evaluated_at": "2019-12-27T18:11:19.117Z",
            "status": "disabled"
          }
        },
        "before": {
          "id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
          "account_id": 1234567,
          "action": "notification",
          "enabled": true,
          "name": "Workers cap",
          "notification_email": "billing@example.com",
          "product_id": "workers",
          "threshold_cents": 100,
          "version": 1,
          "current_state": {
            "balance_cents": 0,
            "billing_period_end": "2019-12-27T18:11:19.117Z",
            "billing_period_start": "2019-12-27T18:11:19.117Z",
            "enforcement": {
              "applied_generation": 0,
              "delivery_status": "pending",
              "desired_generation": 0,
              "desired_state": "active",
              "expires_at": "2019-12-27T18:11:19.117Z"
            },
            "evaluated_at": "2019-12-27T18:11:19.117Z",
            "status": "disabled"
          }
        }
      },
      "occurred_at": "2019-12-27T18:11:19.117Z",
      "policy_id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
      "policy_version": 1,
      "product_id": "product_id"
    }
  ],
  "result_info": {
    "count": 0,
    "cursor": "cursor"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "message": "message",
      "code": 0
    }
  ],
  "messages": [
    {
      "message": "message",
      "code": 0
    }
  ],
  "result": [
    {
      "id": "id",
      "action": "created",
      "actor": "actor",
      "details": {
        "after": {
          "id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
          "account_id": 1234567,
          "action": "notification",
          "enabled": true,
          "name": "Workers cap",
          "notification_email": "billing@example.com",
          "product_id": "workers",
          "threshold_cents": 100,
          "version": 1,
          "current_state": {
            "balance_cents": 0,
            "billing_period_end": "2019-12-27T18:11:19.117Z",
            "billing_period_start": "2019-12-27T18:11:19.117Z",
            "enforcement": {
              "applied_generation": 0,
              "delivery_status": "pending",
              "desired_generation": 0,
              "desired_state": "active",
              "expires_at": "2019-12-27T18:11:19.117Z"
            },
            "evaluated_at": "2019-12-27T18:11:19.117Z",
            "status": "disabled"
          }
        },
        "before": {
          "id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
          "account_id": 1234567,
          "action": "notification",
          "enabled": true,
          "name": "Workers cap",
          "notification_email": "billing@example.com",
          "product_id": "workers",
          "threshold_cents": 100,
          "version": 1,
          "current_state": {
            "balance_cents": 0,
            "billing_period_end": "2019-12-27T18:11:19.117Z",
            "billing_period_start": "2019-12-27T18:11:19.117Z",
            "enforcement": {
              "applied_generation": 0,
              "delivery_status": "pending",
              "desired_generation": 0,
              "desired_state": "active",
              "expires_at": "2019-12-27T18:11:19.117Z"
            },
            "evaluated_at": "2019-12-27T18:11:19.117Z",
            "status": "disabled"
          }
        }
      },
      "occurred_at": "2019-12-27T18:11:19.117Z",
      "policy_id": "6f1c2b8e-3d4a-4f5b-9c6d-7e8f9a0b1c2d",
      "policy_version": 1,
      "product_id": "product_id"
    }
  ],
  "result_info": {
    "count": 0,
    "cursor": "cursor"
  },
  "success": true
}
```