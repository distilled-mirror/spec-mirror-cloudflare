---
title: Produce records
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[K2](https://developers.cloudflare.com/api/resources/k2)

[Data](https://developers.cloudflare.com/api/resources/k2/subresources/data)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Produce records

POST/produce

Send to the stream’s `endpoint`, `https://<stream_id>.k2.cloudflarestorage.com`. Appends a batch of records to the stream. The batch is written atomically, so either every record is stored or none are. Requests are limited to 5 MB, compressed and decompressed, and each record to 1 MB. Gzip bodies are accepted when `Content-Encoding` is `gzip`. Requires an API token with K2 produce permission unless the stream’s HTTP input sets `authentication` to false. Errors use a `success` and `error` body instead of the `errors` array.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Body ParametersJSONExpand Collapse

<details>

<summary>

records: array of object {content, headers }

</summary>

content: string

The record payload, encoded as standard base64. Empty content is valid.

<a href="#">Link to this property</a>

headers: optional map\[string]

Metadata about the record, as string keys and values.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20k2.data%20%3E%20(method)%20produce%20%3E%20(params)%200%20%3E%20(param)%20records%20%3E%20(schema)>)

##### ReturnsExpand Collapse

success: true

[Link to this property](#)%20k2.data%20%3E%20(model)%20data_produce_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Produce records

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl "https://{stream_id}.k2.cloudflarestorage.com/produce" \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "records": [
            {
              "content": "eyJvcmRlcl9pZCI6MTAwMX0="
            }
          ]
        }'
```

200 example

```
{
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "success": true
}
```