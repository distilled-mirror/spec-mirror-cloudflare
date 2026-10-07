---
title: List K2 stream subscriptions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Streams](https://developers.cloudflare.com/api/resources/k2/subresources/streams)

[Subscriptions](https://developers.cloudflare.com/api/resources/k2/subresources/streams/subresources/subscriptions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List K2 stream subscriptions

GET/accounts/{account\_id}/k2/streams/{stream\_id}/subscriptions

Lists every subscription on one stream, oldest first. Lag uses committed positions, not reserved read positions. A failed tail observation preserves subscription metadata and returns unavailable lag.

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

Specifies the public ID of the account.

maxLength32

minLength32

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

stream\_id: string

Specifies the public ID of the K2 stream.

maxLength32

minLength32

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20stream_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, created\_at, lag, 3 more }

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

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Indicates whether the API call was successful.

[Link to this property](#)%20k2.streams.subscriptions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List K2 stream subscriptions

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/k2/streams/$STREAM_ID/subscriptions \
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
      "created_at": "2019-12-27T18:11:19.117Z",
      "lag": {
        "records": "records",
        "status": "available"
      },
      "modified_at": "2019-12-27T18:11:19.117Z",
      "name": "name",
      "start_at": {
        "type": "earliest"
      }
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
      "id": "id",
      "created_at": "2019-12-27T18:11:19.117Z",
      "lag": {
        "records": "records",
        "status": "available"
      },
      "modified_at": "2019-12-27T18:11:19.117Z",
      "name": "name",
      "start_at": {
        "type": "earliest"
      }
    }
  ],
  "success": true
}
```