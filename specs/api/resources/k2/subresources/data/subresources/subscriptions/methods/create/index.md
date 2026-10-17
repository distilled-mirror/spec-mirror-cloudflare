---
title: Create subscription
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

# Create subscription

POST/subscriptions

Send to the stream’s `endpoint`, `https://<stream_id>.k2.cloudflarestorage.com`. Create a subscription, which reads the stream from its own position. Creating a subscription with an existing name returns the existing subscription. A stream can have up to 100 subscriptions. Requires an API token with K2 consume permission.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Body ParametersJSONExpand Collapse

name: string

Specifies the name of the subscription. Creating a subscription with an existing name returns the existing subscription.

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

<details>

<summary>

start\_at: object {type }

</summary>

<details>

<summary>

type: "earliest"or "latest"

Starts at the oldest retained record or at the end of the stream.

</summary>

One of the following:

"earliest"

<a href="#">Link to this property</a>

"latest"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20start_at%20%3E%20(schema)>)

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

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id }

</summary>

id: string

Specifies the ID of the subscription.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Indicates whether the API call was successful.

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create subscription

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl "https://{stream_id}.k2.cloudflarestorage.com/subscriptions" \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "name": "orders_processor",
          "start_at": {
            "type": "earliest"
          }
        }'
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
  "result": {
    "id": "7c1e9b2a4d6f4e8a9b0c1d2e3f4a5b6c"
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
  "result": {
    "id": "7c1e9b2a4d6f4e8a9b0c1d2e3f4a5b6c"
  },
  "success": true
}
```