---
title: Batches
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Data](https://developers.cloudflare.com/api/resources/k2/subresources/data)

[Subscriptions](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Batches

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