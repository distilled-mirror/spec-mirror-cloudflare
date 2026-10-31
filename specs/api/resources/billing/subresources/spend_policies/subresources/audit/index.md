---
title: Audit
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Billing](https://developers.cloudflare.com/api/resources/billing)

[Spend Policies](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Audit

##### [List Spend Policy Audit Entries](https://developers.cloudflare.com/api/resources/billing/subresources/spend_policies/subresources/audit/methods/list)

GET/accounts/{account\_id}/billing/spend-policies/{policy\_id}/audit

##### ModelsExpand Collapse

<details>

<summary>

AuditListResponse object {action, balance\_cents, billing\_period\_end, 7 more }

A state transition recorded when the policy was evaluated against the account’s balance.

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

[Link to this property](#)%20billing.spend_policies.audit%20%3E%20(model)%20audit_list_response%20%3E%20(schema)>)