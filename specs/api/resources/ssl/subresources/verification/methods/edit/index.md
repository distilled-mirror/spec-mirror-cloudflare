---
title: Update SSL Certificate Pack Validation Method
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[SSL](https://developers.cloudflare.com/api/resources/ssl)

[Verification](https://developers.cloudflare.com/api/resources/ssl/subresources/verification)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update SSL Certificate Pack Validation Method

PATCH/zones/{zone\_id}/ssl/verification/{certificate\_pack\_id}

Update the configured SSL validation method for a Universal SSL certificate pack, or request another validation attempt for a pack in pending\_validation. This endpoint does not change the validation method for advanced certificates. For an active certificate pack, a method-only update saves the method without rerunning validation or replacing the active certificate. For a pack pending validation, changing the method initializes validation using the requested method. Cloudflare may select a different method during automatic renewal. Omit validation\_method, send an empty JSON object, or omit the request body to use the current or default method. For a pack in pending\_validation, keeping the current method requests another validation attempt. Cloudflare may queue this attempt rather than complete validation before returning. For an active pack, an empty JSON object or a request without a body does not rerun DCV. The response returns the current status and does not guarantee that validation has completed. Available methods depend on the DNS setup and certificate authority. For Google Trust Services, Let’s Encrypt, and SSL.com, full DNS setups support txt only, while partial DNS setups support txt or http. HTTP validation does not support wildcard certificates. This endpoint allows four PATCH requests per zone per 60 seconds.

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

##### Accepted Permissions (at least one required)

`Access: Mutual TLS Certificates Write``Access: Mutual TLS Certificates Read``SSL and Certificates Write``SSL and Certificates Read`

##### P ath ParametersExpand Collapse

zone\_id: string

Identifier.

maxLength32

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

certificate\_pack\_id: string

Certificate Pack UUID.

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20certificate_pack_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

validation\_method: optional "http"or "cname"or "txt"or "email"

SSL validation method.

</summary>

One of the following:

"http"

<a href="#">Link to this property</a>

"cname"

<a href="#">Link to this property</a>

"txt"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(params)%200%20%3E%20(param)%20validation_method%20%3E%20(schema)>)

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

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {status, validation\_method }

</summary>

status: optional string

Result status.

<a href="#">Link to this property</a>

<details>

<summary>

validation\_method: optional "http"or "cname"or "txt"or "email"

SSL validation method.

</summary>

One of the following:

"http"

<a href="#">Link to this property</a>

"cname"

<a href="#">Link to this property</a>

"txt"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.verification%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Update SSL Certificate Pack Validation Method

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/ssl/verification/$CERTIFICATE_PACK_ID \
    -X PATCH \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
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
  "success": true,
  "result": {
    "status": "pending_validation",
    "validation_method": "txt"
  }
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
  "success": true,
  "result": {
    "status": "pending_validation",
    "validation_method": "txt"
  }
}
```