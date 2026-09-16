---
title: Entitlements
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Accounts](https://developers.cloudflare.com/api/resources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Entitlements

##### [Get Account Entitlements](https://developers.cloudflare.com/api/resources/accounts/subresources/entitlements/methods/list)

GET/accounts/{account\_id}/entitlements

##### ModelsExpand Collapse

<details>

<summary>

EntitlementListResponse object {id, allocation, created\_date, 3 more }

A single entitlement record for a zone or account.

</summary>

id: string

Entitlement identifier — equal to the feature key.

<a href="#">Link to this property</a>

<details>

<summary>

allocation: object {type, value }

Represents the allocation value for an entitlement. The shape of <code>value</code> depends on <code>type</code>: <code>bool</code> uses a boolean, <code>max_count</code> uses an integer, <code>enum_number</code> uses an array of numbers, <code>range</code> uses an object with <code>min</code> and <code>max</code> integer fields, and <code>string</code> uses a string.

</summary>

<details>

<summary>

type: "bool"or "max\_count"or "enum\_number"or 2 more

Allocation type discriminator.

</summary>

One of the following:

"bool"

<a href="#">Link to this property</a>

"max\_count"

<a href="#">Link to this property</a>

"enum\_number"

<a href="#">Link to this property</a>

"range"

<a href="#">Link to this property</a>

"string"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

Contains the allocation value whose concrete type the <code>type</code> field determines: bool yields a boolean, max\_count yields an integer, enum\_number yields an array of numbers, range yields an object with <code>min</code> and <code>max</code>, and string yields a string.

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

array of number

<a href="#">Link to this property</a>

<details>

<summary>

object {max, min }

</summary>

max: number

<a href="#">Link to this property</a>

min: number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_date: string

ISO 8601 timestamp (microsecond precision, no timezone offset) when the entitlement was created. Format: <code>YYYY-MM-DDTHH:MM:SS.ffffff</code>.

<a href="#">Link to this property</a>

deleted\_date: string

ISO 8601 timestamp when the entitlement was deleted, or empty string if not deleted.

<a href="#">Link to this property</a>

edited\_date: string

ISO 8601 timestamp (microsecond precision, no timezone offset) when the entitlement was last edited.

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {id, feature\_set, key, name }

Describes a product feature associated with an entitlement.

</summary>

id: number

Numeric identifier of the feature.

formatint64

<a href="#">Link to this property</a>

feature\_set: string

The logical grouping (set) this feature belongs to.

<a href="#">Link to this property</a>

key: string

Unique string key for the feature.

<a href="#">Link to this property</a>

name: string

Human-readable name of the feature.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20accounts.entitlements%20%3E%20(model)%20entitlement_list_response%20%3E%20(schema)>)