---
title: List K2 streams
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Streams](https://developers.cloudflare.com/api/resources/k2/subresources/streams)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List K2 streams

GET/accounts/{account\_id}/k2/streams

List or filter K2 streams in an account.

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

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

name: optional string

Filters K2 streams by name using a case-insensitive substring.

maxLength128

minLength1

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20name%20%3E%20(schema)>)

page: optional number

minimum1

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

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

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, created\_at, endpoint, 5 more }

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

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, page, per\_page, total\_count }

</summary>

count: number

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: boolean

Indicates whether the API call was successful.

[Link to this property](#)%20k2.streams%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List K2 streams

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/k2/streams \
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
      "id": "053e105f4ecef8ad9ca31a8372d0c353",
      "created_at": "2019-12-27T18:11:19.117Z",
      "endpoint": "https://053e105f4ecef8ad9ca31a8372d0c353.k2.cloudflarestorage.com",
      "http": {
        "enabled": true,
        "authentication": true,
        "cors": {
          "origins": [
            "string"
          ]
        }
      },
      "modified_at": "2019-12-27T18:11:19.117Z",
      "name": "my_k2_stream",
      "retention_seconds": 604800,
      "worker_binding": {
        "enabled": false
      }
    }
  ],
  "result_info": {
    "count": 0,
    "page": 0,
    "per_page": 0,
    "total_count": 0
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
      "id": "053e105f4ecef8ad9ca31a8372d0c353",
      "created_at": "2019-12-27T18:11:19.117Z",
      "endpoint": "https://053e105f4ecef8ad9ca31a8372d0c353.k2.cloudflarestorage.com",
      "http": {
        "enabled": true,
        "authentication": true,
        "cors": {
          "origins": [
            "string"
          ]
        }
      },
      "modified_at": "2019-12-27T18:11:19.117Z",
      "name": "my_k2_stream",
      "retention_seconds": 604800,
      "worker_binding": {
        "enabled": false
      }
    }
  ],
  "result_info": {
    "count": 0,
    "page": 0,
    "per_page": 0,
    "total_count": 0
  },
  "success": true
}
```