---
title: Validate a custom page template
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Custom Pages](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/custom_pages)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Validate a custom page template

POST/accounts/{account\_id}/access/custom\_pages/validate

Validate a Liquid template and return its errors and warnings without persisting it.

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

`Access: Custom Pages Write`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

template: string

The Liquid template to validate.

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20template%20%3E%20(schema)>)

<details>

<summary>

type: "identity\_denied"or "forbidden"or "login"or "interstitial"

Custom page type.

</summary>

One of the following:

"identity\_denied"

<a href="#">Link to this property</a>

"forbidden"

<a href="#">Link to this property</a>

"login"

<a href="#">Link to this property</a>

"interstitial"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20type%20%3E%20(schema)>)

version: optional number

Contract version to validate against; omit for the latest.

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20version%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {errors, page\_type, version, warnings }

The result of validating a template’s content.

</summary>

<details>

<summary>

errors: array of object {message, tier, ref }

Blocking findings; a non-empty list means the template cannot be published.

</summary>

message: string

Human-readable description of the finding.

<a href="#">Link to this property</a>

tier: string

The validation tier that produced the finding (e.g. html, liquid).

<a href="#">Link to this property</a>

ref: optional string

Optional pointer to the part of the template the finding refers to.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

page\_type: "identity\_denied"or "forbidden"or "login"or "interstitial"

Custom page type.

</summary>

One of the following:

"identity\_denied"

<a href="#">Link to this property</a>

"forbidden"

<a href="#">Link to this property</a>

"login"

<a href="#">Link to this property</a>

"interstitial"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: number

The contract version the template was validated against.

<a href="#">Link to this property</a>

<details>

<summary>

warnings: array of object {message, tier, ref }

Advisory findings that do not block publishing.

</summary>

message: string

Human-readable description of the finding.

<a href="#">Link to this property</a>

tier: string

The validation tier that produced the finding (e.g. html, liquid).

<a href="#">Link to this property</a>

ref: optional string

Optional pointer to the part of the template the finding refers to.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.custom_pages%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Validate a custom page template

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/custom_pages/validate \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "template": "template",
          "type": "identity_denied"
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
    "errors": [
      {
        "message": "message",
        "tier": "tier",
        "ref": "ref"
      }
    ],
    "page_type": "identity_denied",
    "version": 0,
    "warnings": [
      {
        "message": "message",
        "tier": "tier",
        "ref": "ref"
      }
    ]
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
    "errors": [
      {
        "message": "message",
        "tier": "tier",
        "ref": "ref"
      }
    ],
    "page_type": "identity_denied",
    "version": 0,
    "warnings": [
      {
        "message": "message",
        "tier": "tier",
        "ref": "ref"
      }
    ]
  }
}
```