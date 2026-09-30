---
title: Prepare a container image
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Images](https://developers.cloudflare.com/api/resources/containers/subresources/images)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Prepare a container image

POST/accounts/{account\_id}/containers/image-preparations

Idempotently starts or observes preparation of the runtime artifacts required to run one digest-pinned managed container image on Cloudflare’s network. Returns 202 while durable preparation continues and 200 when the image is ready or preparation has reached a terminal error.

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

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

image: string

Image url.

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(params)%200%20%3E%20(param)%20image%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {image, status, artifact\_digest, reason }

Durable preparation state for a container image.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "ready"or "error"

Current durable preparation state for a container image.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

artifact\_digest: optional string

Digest of the prepared runtime artifact when status is ready.

<a href="#">Link to this property</a>

reason: optional string

Human-readable pending or terminal error detail.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.images%20%3E%20(method)%20prepare%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Prepare a container image

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/image-preparations \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "image": "image"
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "image": "image",
    "status": "pending",
    "artifact_digest": "artifact_digest",
    "reason": "reason"
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
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "image": "image",
    "status": "pending",
    "artifact_digest": "artifact_digest",
    "reason": "reason"
  },
  "success": true
}
```