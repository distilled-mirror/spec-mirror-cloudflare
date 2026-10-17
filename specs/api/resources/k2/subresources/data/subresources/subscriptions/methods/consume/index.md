---
title: Consume records
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

# Consume records

POST/subscriptions/{subscription\_id}/consume

Send to the stream’s `endpoint`, `https://<stream_id>.k2.cloudflarestorage.com`. Returns the next batch of records and leases it to the worker for 5 minutes. ACK the batch after processing it, NACK it to have it redelivered, or extend the lease if processing takes longer. When no records are available, the response has no records and a null `batch_id`. Returns 429 with code 10216 when every parallel read slot for the subscription is leased, and 409 with code 10217 while this worker has a read in progress; retry both. Requires an API token with K2 consume permission.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

subscription\_id: string

Specifies the ID of the subscription.

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(params)%20default%20%3E%20(param)%20subscription_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

max\_records: number

Sets the maximum number of records to return.

maximum10000

minimum1

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(params)%200%20%3E%20(param)%20max_records%20%3E%20(schema)>)

worker\_id: string

Identifies the consumer process. Each worker holds at most one batch at a time.

maxLength256

minLength1

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(params)%200%20%3E%20(param)%20worker_id%20%3E%20(schema)>)

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

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {batch\_id, leased\_until\_ms, records }

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

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Indicates whether the API call was successful.

[Link to this property](#)%20k2.data.subscriptions%20%3E%20(method)%20consume%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Consume records

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl "https://{stream_id}.k2.cloudflarestorage.com/subscriptions/$SUBSCRIPTION_ID/consume" \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "max_records": 100,
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
  "result": {
    "batch_id": "batch_id",
    "leased_until_ms": 1759737900000,
    "records": [
      {
        "content": "eyJvcmRlcl9pZCI6MTAwMX0=",
        "timestamp_ms": 1759737600000,
        "headers": {
          "foo": "string"
        }
      }
    ]
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
    "batch_id": "batch_id",
    "leased_until_ms": 1759737900000,
    "records": [
      {
        "content": "eyJvcmRlcl9pZCI6MTAwMX0=",
        "timestamp_ms": 1759737600000,
        "headers": {
          "foo": "string"
        }
      }
    ]
  },
  "success": true
}
```