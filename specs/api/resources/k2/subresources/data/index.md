---
title: Data
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Data

##### [Produce records](https://developers.cloudflare.com/api/resources/k2/subresources/data/methods/produce)

POST/produce

##### ModelsExpand Collapse

<details>

<summary>

DataProduceResponse object {success }

</summary>

success: true

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data%20%3E%20(model)%20data_produce_response%20%3E%20(schema)>)

#### DataSubscriptions

##### [List subscriptions](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/methods/list)

GET/subscriptions

##### [Create subscription](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/methods/create)

POST/subscriptions

##### [Get subscription](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/methods/get)

GET/subscriptions/{subscription\_id}

##### [Delete subscription](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/methods/delete)

DELETE/subscriptions/{subscription\_id}

##### [Consume records](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/methods/consume)

POST/subscriptions/{subscription\_id}/consume

##### ModelsExpand Collapse

<details>

<summary>

SubscriptionListResponse object {id, created\_at, modified\_at, 2 more }

</summary>

id: string

Specifies the ID of the subscription.

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

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

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(model)%20subscription_list_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionCreateResponse object {id }

</summary>

id: string

Specifies the ID of the subscription.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(model)%20subscription_create_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionGetResponse object {id, created\_at, modified\_at, 2 more }

</summary>

id: string

Specifies the ID of the subscription.

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

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

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(model)%20subscription_get_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionDeleteResponse object {id }

</summary>

id: string

Specifies the ID of the subscription.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(model)%20subscription_delete_response%20%3E%20(schema)>)

<details>

<summary>

SubscriptionConsumeResponse object {batch\_id, leased\_until\_ms, records }

</summary>

batch\_id: string

Identifies the delivered batch for ACK, NACK, and extend. Null when the response contains no records.

<a href="#">Link to this property</a>

leased\_until\_ms: number

Shows when the lease on the batch expires, in epoch milliseconds. ACK or NACK the batch before then. Null when the response contains no records.

<a href="#">Link to this property</a>

<details>

<summary>

records: array of object {content, timestamp\_ms, headers }

</summary>

content: string

The record payload, encoded as standard base64.

formatbyte

<a href="#">Link to this property</a>

timestamp\_ms: number

Shows when K2 received the record, in epoch milliseconds.

<a href="#">Link to this property</a>

headers: optional map\[string]

Lists the metadata the producer attached to the record. Omitted when the record carries none.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(model)%20subscription_consume_response%20%3E%20(schema)>)

#### DataSubscriptionsBatches

##### [Acknowledge batch](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/subresources/batches/methods/ack)

POST/subscriptions/{subscription\_id}/batches/{batch\_id}/ack

##### [Release batch](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/subresources/batches/methods/nack)

POST/subscriptions/{subscription\_id}/batches/{batch\_id}/nack

##### [Extend batch lease](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/subresources/batches/methods/extend)

POST/subscriptions/{subscription\_id}/batches/{batch\_id}/extend

##### ModelsExpand Collapse

BatchAckResponse = unknown

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(model)%20batch_ack_response%20%3E%20(schema)>)

BatchNackResponse = unknown

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(model)%20batch_nack_response%20%3E%20(schema)>)

<details>

<summary>

BatchExtendResponse object {leased\_until\_ms }

</summary>

leased\_until\_ms: number

Shows the new lease expiry, in epoch milliseconds.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(model)%20batch_extend_response%20%3E%20(schema)>)