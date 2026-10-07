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