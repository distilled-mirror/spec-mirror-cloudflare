---
title: Release batch
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Data](https://developers.cloudflare.com/api/resources/k2/subresources/data)

[Subscriptions](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions)

[Batches](https://developers.cloudflare.com/api/resources/k2/subresources/data/subresources/subscriptions/subresources/batches)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Release batch

POST/subscriptions/{subscription\_id}/batches/{batch\_id}/nack

Send to the stream’s `endpoint`, `https://<stream_id>.k2.cloudflarestorage.com`. Returns a batch to the subscription for redelivery. The next Consume request from any worker receives them under a new `batch_id`. Releasing an unknown or already settled batch also succeeds. Requires an API token with K2 consume permission.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

subscription\_id: string

Specifies the ID of the subscription.

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(params)%20default%20%3E%20(param)%20subscription_id%20%3E%20(schema)>)

batch\_id: string

Specifies the ID of a delivered batch, from the Consume response.

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(params)%20default%20%3E%20(param)%20batch_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

worker\_id: string

Identifies the consumer process. Each worker holds at most one batch at a time.

maxLength256

minLength1

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(params)%200%20%3E%20(param)%20worker_id%20%3E%20(schema)>)

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

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

result: unknown

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Indicates whether the API call was successful.

[Link to this property](#)%20k2.data.subscriptions.batches%20%3E%20(method)%20nack%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Release batch

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl "https://{stream_id}.k2.cloudflarestorage.com/subscriptions/$SUBSCRIPTION_ID/batches/$BATCH_ID/nack" \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "worker_id": "worker-1"
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
  "result": {},
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
  "result": {},
  "success": true
}
```