---
title: Update a DLS prefix binding
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Data Localization Suite](https://developers.cloudflare.com/api/resources/dls)

[Regional Services](https://developers.cloudflare.com/api/resources/dls/subresources/regional_services)

[Prefix Bindings](https://developers.cloudflare.com/api/resources/dls/subresources/regional_services/subresources/prefix_bindings)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update a DLS prefix binding

PATCH/accounts/{account\_id}/dls/regional\_services/prefix\_bindings/{binding\_id}

Update the region of an existing BYOIP prefix binding.

Like creating a binding, this requires **IP Prefixes Write** in addition to **DLS Write**.

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

`DLS: Write``IP Prefixes: Write`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier of a Cloudflare account.

maxLength32

minLength32

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

binding\_id: string

Unique identifier for the prefix binding.

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20binding_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

region\_key: string

New region key to assign (e.g., “us”, “eu”, “cfcanary”).

maxLength128

minLength1

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(params)%200%20%3E%20(param)%20region_key%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

messages: array of object {code, message, error\_chain }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

error\_chain: optional array of unknown

Optional upstream error context for APIv4 errors that wrap downstream service failures.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, cidr, prefix\_id, region\_key }

</summary>

id: string

The ID of the binding.

<a href="#">Link to this property</a>

cidr: string

The CIDR that is bound.

<a href="#">Link to this property</a>

prefix\_id: string

The ID of the parent prefix.

<a href="#">Link to this property</a>

region\_key: string

The region key used for the binding.

maxLength128

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

errors: optional array of object {code, message, error\_chain }

maxLength0

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

error\_chain: optional array of unknown

Optional upstream error context for APIv4 errors that wrap downstream service failures.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dls.regional_services.prefix_bindings%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

### Update a DLS prefix binding

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/dls/regional_services/prefix_bindings/$BINDING_ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "region_key": "eu"
        }'
```

200 example

```
{
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "error_chain": [
        {}
      ]
    }
  ],
  "result": {
    "id": "id",
    "cidr": "cidr",
    "prefix_id": "prefix_id",
    "region_key": "x"
  },
  "success": true,
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "error_chain": [
        {}
      ]
    }
  ]
}
```

##### Returns Examples

200 example

```
{
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "error_chain": [
        {}
      ]
    }
  ],
  "result": {
    "id": "id",
    "cidr": "cidr",
    "prefix_id": "prefix_id",
    "region_key": "x"
  },
  "success": true,
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "error_chain": [
        {}
      ]
    }
  ]
}
```