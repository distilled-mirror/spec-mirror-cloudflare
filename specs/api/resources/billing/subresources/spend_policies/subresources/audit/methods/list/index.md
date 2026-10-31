---
title: List Spend Policy Audit Entries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Billing](https://developers.cloudflare.com/api/resources/billing)

[Spend Policies](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies)

[Audit](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies/subresources/audit)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Spend Policy Audit Entries

GET/accounts/{account\_id}/billing/spend-policies/{policy\_id}/audit

Returns the policy’s evaluation history, newest first. At most one entry is recorded per trigger (`approaching_limit` or `limit_reached`), policy version and billing period, so a policy update can record a new entry without any change in balance. Disabled policies still return their history; deleted policies return `404`. There is no pagination: use `limit` to set how many entries come back.

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

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

policy\_id: string

The unique identifier of the spend policy.

formatuuid

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20policy_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

limit: optional number

Maximum number of audit entries to return. Defaults to 50. Values above 100 are capped at 100 rather than rejected.

minimum1

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

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

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {action, balance\_cents, billing\_period\_end, 7 more }

Audit entries, newest first. An empty array when there are none.

</summary>

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

balance\_cents: number

The account’s balance for the product at evaluation time, in US cents.

formatint64

<a href="#">Link to this property</a>

billing\_period\_end: string

Exclusive end of the billing period that was evaluated.

formatdate-time

<a href="#">Link to this property</a>

billing\_period\_start: string

Inclusive start of the billing period that was evaluated.

formatdate-time

<a href="#">Link to this property</a>

created\_at: string

When the entry was recorded.

formatdate-time

<a href="#">Link to this property</a>

policy\_version: number

The policy <code>version</code> that was evaluated.

formatint64

<a href="#">Link to this property</a>

reason: string

A human-readable explanation of the trigger.

<a href="#">Link to this property</a>

<details>

<summary>

source: "kafka"or "policy\_revision"

What caused the evaluation. <code>kafka</code> means a balance update. <code>policy_revision</code> means a change to the policy.

</summary>

One of the following:

"kafka"

<a href="#">Link to this property</a>

"policy\_revision"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

threshold\_cents: number

The policy threshold at evaluation time, in US cents.

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

trigger: "approaching\_limit"or "limit\_reached"

The state the balance moved into. <code>approaching_limit</code> means the balance is at least 80% of the threshold (rounded up to a whole cent), but below the threshold. <code>limit_reached</code> means the balance reached or exceeded the threshold.

</summary>

One of the following:

"approaching\_limit"

<a href="#">Link to this property</a>

"limit\_reached"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Indicates whether the API call was successful.

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Spend Policy Audit Entries

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/billing/spend-policies/$POLICY_ID/audit \
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
      "action": "notification",
      "balance_cents": 104,
      "billing_period_end": "2026-11-01T00:00:00Z",
      "billing_period_start": "2026-10-01T00:00:00Z",
      "created_at": "2026-10-14T12:34:56Z",
      "policy_version": 2,
      "reason": "balance reached or exceeded the configured threshold",
      "source": "kafka",
      "threshold_cents": 100,
      "trigger": "limit_reached"
    }
  ],
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
      "action": "notification",
      "balance_cents": 104,
      "billing_period_end": "2026-11-01T00:00:00Z",
      "billing_period_start": "2026-10-01T00:00:00Z",
      "created_at": "2026-10-14T12:34:56Z",
      "policy_version": 2,
      "reason": "balance reached or exceeded the configured threshold",
      "source": "kafka",
      "threshold_cents": 100,
      "trigger": "limit_reached"
    }
  ],
  "success": true
}
```