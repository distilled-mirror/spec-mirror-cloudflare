---
title: Order Advanced Certificate Manager Certificate Pack
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[SSL](https://developers.cloudflare.com/api/resources/ssl)

[Certificate Packs](https://developers.cloudflare.com/api/resources/ssl/subresources/certificate_packs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Order Advanced Certificate Manager Certificate Pack

POST/zones/{zone\_id}/ssl/certificate\_packs/order

For a given zone, order an advanced certificate pack.

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

`SSL and Certificates Write`

##### P ath ParametersExpand Collapse

zone\_id: string

Identifier.

maxLength32

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

certificate\_authority: "google"or "lets\_encrypt"or "ssl\_com"

Certificate Authority selected for the order. For information on any certificate authority specific details or restrictions <a href="https://developers.cloudflare.com/ssl/reference/certificate-authorities">see this page for more details</a>.

</summary>

One of the following:

"google"

<a href="#">Link to this property</a>

"lets\_encrypt"

<a href="#">Link to this property</a>

"ssl\_com"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20certificate_authority%20%3E%20(schema)>)

hosts: array of [Host](<https://developers.cloudflare.com/api/resources/ssl#(resource)%20ssl.certificate_packs%20%3E%20(model)%20host%20%3E%20(schema)>)

Comma separated list of valid host names for the certificate packs. Must contain the zone apex, may not contain more than 50 hosts, and may not be empty.

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20hosts%20%3E%20(schema)>)

type: "advanced"

Type of certificate pack.

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20type%20%3E%20(schema)>)

<details>

<summary>

validation\_method: "txt"or "http"or "email"

Validation Method selected for the order.

</summary>

One of the following:

"txt"

<a href="#">Link to this property</a>

"http"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20validation_method%20%3E%20(schema)>)

<details>

<summary>

validity\_days: 14or 30or 90or 365

Validity Days selected for the order.

</summary>

One of the following:

14

<a href="#">Link to this property</a>

30

<a href="#">Link to this property</a>

90

<a href="#">Link to this property</a>

365

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20validity_days%20%3E%20(schema)>)

cloudflare\_branding: optional boolean

Whether or not to add Cloudflare Branding for the order. This will add a subdomain of sni.cloudflaressl.com as the Common Name if set to true.

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20cloudflare_branding%20%3E%20(schema)>)

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

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {id, hosts, status, 4 more }

A newly ordered certificate pack. Certificates are not included until they are issued; get the certificate pack to retrieve them.

</summary>

id: string

The unique identifier for a certificate\_pack.

<a href="#">Link to this property</a>

hosts: array of <a href="https://developers.cloudflare.com/api/resources/ssl#(resource)%20ssl.certificate_packs%20%3E%20(model)%20host%20%3E%20(schema)">Host</a>

Comma separated list of valid host names for the certificate packs. Must contain the zone apex, may not contain more than 50 hosts, and may not be empty.

<a href="#">Link to this property</a>

<details>

<summary>

status: <a href="https://developers.cloudflare.com/api/resources/ssl#(resource)%20ssl.certificate_packs%20%3E%20(model)%20status%20%3E%20(schema)">Status</a>

Status of certificate pack.

</summary>

One of the following:

"initializing"

<a href="#">Link to this property</a>

"pending\_validation"

<a href="#">Link to this property</a>

"deleted"

<a href="#">Link to this property</a>

"pending\_issuance"

<a href="#">Link to this property</a>

"pending\_deployment"

<a href="#">Link to this property</a>

"pending\_deletion"

<a href="#">Link to this property</a>

"pending\_expiration"

<a href="#">Link to this property</a>

"expired"

<a href="#">Link to this property</a>

"active"

<a href="#">Link to this property</a>

"initializing\_timed\_out"

<a href="#">Link to this property</a>

"validation\_timed\_out"

<a href="#">Link to this property</a>

"issuance\_timed\_out"

<a href="#">Link to this property</a>

"deployment\_timed\_out"

<a href="#">Link to this property</a>

"deletion\_timed\_out"

<a href="#">Link to this property</a>

"pending\_cleanup"

<a href="#">Link to this property</a>

"staging\_deployment"

<a href="#">Link to this property</a>

"staging\_active"

<a href="#">Link to this property</a>

"deactivating"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

"backup\_issued"

<a href="#">Link to this property</a>

"holding\_deployment"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "mh\_custom"or "managed\_hostname"or "sni\_custom"or 5 more

Type of certificate pack.

</summary>

One of the following:

"mh\_custom"

<a href="#">Link to this property</a>

"managed\_hostname"

<a href="#">Link to this property</a>

"sni\_custom"

<a href="#">Link to this property</a>

"universal"

<a href="#">Link to this property</a>

"advanced"

<a href="#">Link to this property</a>

"total\_tls"

<a href="#">Link to this property</a>

"keyless"

<a href="#">Link to this property</a>

"legacy\_custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

certificate\_authority: optional "google"or "lets\_encrypt"or "ssl\_com"

Certificate Authority selected for the order. For information on any certificate authority specific details or restrictions <a href="https://developers.cloudflare.com/ssl/reference/certificate-authorities">see this page for more details</a>.

</summary>

One of the following:

"google"

<a href="#">Link to this property</a>

"lets\_encrypt"

<a href="#">Link to this property</a>

"ssl\_com"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

validation\_method: optional "txt"or "http"or "email"

Validation Method selected for the order.

</summary>

One of the following:

"txt"

<a href="#">Link to this property</a>

"http"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

validity\_days: optional 14or 30or 90or 365

Validity Days selected for the order.

</summary>

One of the following:

14

<a href="#">Link to this property</a>

30

<a href="#">Link to this property</a>

90

<a href="#">Link to this property</a>

365

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ssl.certificate_packs%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Order Advanced Certificate Manager Certificate Pack

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/ssl/certificate_packs/order \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "certificate_authority": "lets_encrypt",
          "hosts": [
            "example.com",
            "*.example.com",
            "www.example.com"
          ],
          "type": "advanced",
          "validation_method": "txt",
          "validity_days": 14
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
  "success": true,
  "result": {
    "id": "3822ff90-ea29-44df-9e55-21300bb9419b",
    "hosts": [
      "example.com",
      "*.example.com",
      "www.example.com"
    ],
    "status": "initializing",
    "type": "universal",
    "certificate_authority": "lets_encrypt",
    "validation_method": "txt",
    "validity_days": 14
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
    "id": "3822ff90-ea29-44df-9e55-21300bb9419b",
    "hosts": [
      "example.com",
      "*.example.com",
      "www.example.com"
    ],
    "status": "initializing",
    "type": "universal",
    "certificate_authority": "lets_encrypt",
    "validation_method": "txt",
    "validity_days": 14
  }
}
```