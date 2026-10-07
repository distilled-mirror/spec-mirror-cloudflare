---
title: Subscriptions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Streams](https://developers.cloudflare.com/api/resources/k2/subresources/streams)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Subscriptions

##### [List K2 stream subscriptions](https://developers.cloudflare.com/api/resources/k2/subresources/streams/subresources/subscriptions/methods/list)

GET/accounts/{account\_id}/k2/streams/{stream\_id}/subscriptions

##### ModelsExpand Collapse

<details>

<summary>

SubscriptionListResponse object {id, created\_at, lag, 3 more }

</summary>

id: string

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

lag: object {records, status }

</summary>

records: string

Decimal-string distance from the subscription’s committed position to the observed exclusive stream tail, in records. Includes in-flight records and may include expired records or records acknowledged beyond an earlier gap. Null unless status is available.

<a href="#">Link to this property</a>

<details>

<summary>

status: "available"or "unsupported"or "unavailable"

Unsupported means the subscription or stream topology cannot be measured; unavailable means a required observation failed or was inconsistent.

</summary>

One of the following:

"available"

<a href="#">Link to this property</a>

"unsupported"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

<details>

<summary>

start\_at: object {type }

</summary>

<details>

<summary>

type: "earliest"or "latest"

</summary>

One of the following:

"earliest"

<a href="#">Link to this property</a>

"latest"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(model)%20subscription_list_response%20%3E%20(schema)>)