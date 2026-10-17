---
title: K2
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# K2

#### K2Streams

##### [List K2 streams](https://developers.cloudflare.com/api/resources/k2/subresources/streams/methods/list)

GET/accounts/{account\_id}/k2/streams

##### [Get K2 stream](https://developers.cloudflare.com/api/resources/k2/subresources/streams/methods/get)

GET/accounts/{account\_id}/k2/streams/{stream\_id}

##### [Create K2 stream](https://developers.cloudflare.com/api/resources/k2/subresources/streams/methods/create)

POST/accounts/{account\_id}/k2/streams

##### [Update K2 stream](https://developers.cloudflare.com/api/resources/k2/subresources/streams/methods/update)

PATCH/accounts/{account\_id}/k2/streams/{stream\_id}

##### [Delete K2 stream](https://developers.cloudflare.com/api/resources/k2/subresources/streams/methods/delete)

DELETE/accounts/{account\_id}/k2/streams/{stream\_id}

##### ModelsExpand Collapse

<details>

<summary>

StreamListResponse object {id, created\_at, endpoint, 5 more }

</summary>

id: string

Specifies the public ID of the K2 stream.

maxLength32

minLength32

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

endpoint: string

Indicates the base HTTP endpoint for producing and consuming records.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

http: object {enabled, authentication, cors }

Configures the HTTP endpoint. Disabling HTTP keeps <code>authentication</code> and <code>cors</code>, so enabling it again restores them.

</summary>

enabled: boolean

Indicates whether the HTTP endpoint accepts records.

<a href="#">Link to this property</a>

authentication: optional boolean

Indicates whether the HTTP endpoint requires an API token with K2 produce permission. When false, the endpoint accepts unauthenticated records. Defaults to true when HTTP is enabled without a stored value.

<a href="#">Link to this property</a>

<details>

<summary>

cors: optional object {origins }

</summary>

origins: optional array of string

Allows browser requests from these HTTP or HTTPS origins. Use a wildcard only as the sole origin. An empty list blocks cross-origin browser requests. Defaults to <code>['*']</code> when HTTP is enabled without stored origins.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Indicates the name of the K2 stream.

maxLength128

minLength1

<a href="#">Link to this property</a>

retention\_seconds: number

Shows the configured record retention period from 1 hour (3600 seconds) to 30 days (2592000 seconds), inclusive.

maximum2592000

minimum3600

<a href="#">Link to this property</a>

<details>

<summary>

worker\_binding: object {enabled } or object {enabled }

</summary>

One of the following:

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: false

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: true

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(model)%20stream_list_response%20%3E%20(schema)>)

<details>

<summary>

StreamGetResponse object {id, created\_at, endpoint, 5 more }

</summary>

id: string

Specifies the public ID of the K2 stream.

maxLength32

minLength32

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

endpoint: string

Indicates the base HTTP endpoint for producing and consuming records.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

http: object {enabled, authentication, cors }

Configures the HTTP endpoint. Disabling HTTP keeps <code>authentication</code> and <code>cors</code>, so enabling it again restores them.

</summary>

enabled: boolean

Indicates whether the HTTP endpoint accepts records.

<a href="#">Link to this property</a>

authentication: optional boolean

Indicates whether the HTTP endpoint requires an API token with K2 produce permission. When false, the endpoint accepts unauthenticated records. Defaults to true when HTTP is enabled without a stored value.

<a href="#">Link to this property</a>

<details>

<summary>

cors: optional object {origins }

</summary>

origins: optional array of string

Allows browser requests from these HTTP or HTTPS origins. Use a wildcard only as the sole origin. An empty list blocks cross-origin browser requests. Defaults to <code>['*']</code> when HTTP is enabled without stored origins.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Indicates the name of the K2 stream.

maxLength128

minLength1

<a href="#">Link to this property</a>

retention\_seconds: number

Shows the configured record retention period from 1 hour (3600 seconds) to 30 days (2592000 seconds), inclusive.

maximum2592000

minimum3600

<a href="#">Link to this property</a>

<details>

<summary>

worker\_binding: object {enabled } or object {enabled }

</summary>

One of the following:

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: false

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: true

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(model)%20stream_get_response%20%3E%20(schema)>)

<details>

<summary>

StreamCreateResponse object {id, created\_at, endpoint, 5 more }

</summary>

id: string

Specifies the public ID of the K2 stream.

maxLength32

minLength32

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

endpoint: string

Indicates the base HTTP endpoint for producing and consuming records.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

http: object {enabled, authentication, cors }

Configures the HTTP endpoint. Disabling HTTP keeps <code>authentication</code> and <code>cors</code>, so enabling it again restores them.

</summary>

enabled: boolean

Indicates whether the HTTP endpoint accepts records.

<a href="#">Link to this property</a>

authentication: optional boolean

Indicates whether the HTTP endpoint requires an API token with K2 produce permission. When false, the endpoint accepts unauthenticated records. Defaults to true when HTTP is enabled without a stored value.

<a href="#">Link to this property</a>

<details>

<summary>

cors: optional object {origins }

</summary>

origins: optional array of string

Allows browser requests from these HTTP or HTTPS origins. Use a wildcard only as the sole origin. An empty list blocks cross-origin browser requests. Defaults to <code>['*']</code> when HTTP is enabled without stored origins.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Indicates the name of the K2 stream.

maxLength128

minLength1

<a href="#">Link to this property</a>

retention\_seconds: number

Shows the configured record retention period from 1 hour (3600 seconds) to 30 days (2592000 seconds), inclusive.

maximum2592000

minimum3600

<a href="#">Link to this property</a>

<details>

<summary>

worker\_binding: object {enabled } or object {enabled }

</summary>

One of the following:

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: false

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: true

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(model)%20stream_create_response%20%3E%20(schema)>)

<details>

<summary>

StreamUpdateResponse object {id, created\_at, endpoint, 5 more }

</summary>

id: string

Specifies the public ID of the K2 stream.

maxLength32

minLength32

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

endpoint: string

Indicates the base HTTP endpoint for producing and consuming records.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

http: object {enabled, authentication, cors }

Configures the HTTP endpoint. Disabling HTTP keeps <code>authentication</code> and <code>cors</code>, so enabling it again restores them.

</summary>

enabled: boolean

Indicates whether the HTTP endpoint accepts records.

<a href="#">Link to this property</a>

authentication: optional boolean

Indicates whether the HTTP endpoint requires an API token with K2 produce permission. When false, the endpoint accepts unauthenticated records. Defaults to true when HTTP is enabled without a stored value.

<a href="#">Link to this property</a>

<details>

<summary>

cors: optional object {origins }

</summary>

origins: optional array of string

Allows browser requests from these HTTP or HTTPS origins. Use a wildcard only as the sole origin. An empty list blocks cross-origin browser requests. Defaults to <code>['*']</code> when HTTP is enabled without stored origins.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Indicates the name of the K2 stream.

maxLength128

minLength1

<a href="#">Link to this property</a>

retention\_seconds: number

Shows the configured record retention period from 1 hour (3600 seconds) to 30 days (2592000 seconds), inclusive.

maximum2592000

minimum3600

<a href="#">Link to this property</a>

<details>

<summary>

worker\_binding: object {enabled } or object {enabled }

</summary>

One of the following:

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: false

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

Enabled object {enabled }

</summary>

enabled: true

Indicates whether Workers bindings can produce records to the stream.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(model)%20stream_update_response%20%3E%20(schema)>)

StreamDeleteResponse = unknown

[Link to this property](#)%20k2.streams%20%3E%20(model)%20stream_delete_response%20%3E%20(schema)>)

#### K2StreamsSubscriptions

##### [List subscriptions with consumer lag](https://developers.cloudflare.com/api/resources/k2/subresources/streams/subresources/subscriptions/methods/list)

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

#### K2Data

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

#### K2DataSubscriptions

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

#### K2DataSubscriptionsBatches

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