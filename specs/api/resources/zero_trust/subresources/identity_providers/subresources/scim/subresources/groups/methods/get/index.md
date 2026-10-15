---
title: Get a SCIM Group resource
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Identity Providers](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers)

[SCIM](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim)

[Groups](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a SCIM Group resource

GET/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups/{group\_id}

Returns a SCIM Group resource, including its direct members, synced to Cloudflare via the System for Cross-domain Identity Management (SCIM).

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

`Access: Organizations, Identity Providers, and Groups Write``Access: Organizations, Identity Providers, and Groups Read`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

identity\_provider\_id: string

UUID.

maxLength36

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20identity_provider_id%20%3E%20(schema)>)

group\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20group_id%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {id, displayName, externalId, 3 more }

</summary>

id: optional string

The unique Cloudflare-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

displayName: optional string

The display name of the SCIM Group resource.

<a href="#">Link to this property</a>

externalId: optional string

The IdP-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {value, "$ref", display, type }

The direct members of the SCIM Group resource.

</summary>

value: string

The unique Cloudflare-generated Id of the member resource.

<a href="#">Link to this property</a>

"$ref": optional string

The URI of the member resource.

formaturi

<a href="#">Link to this property</a>

display: optional string

The display name of the member resource.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "User"or "Group"

The SCIM resource type of the member.

</summary>

One of the following:

"User"

<a href="#">Link to this property</a>

"Group"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified }

The metadata of the SCIM resource.

</summary>

created: optional string

The timestamp of when the SCIM resource was created.

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

The timestamp of when the SCIM resource was last modified.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The list of URIs which indicate the attributes contained within a SCIM resource.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Get a SCIM Group resource

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/identity_providers/$IDENTITY_PROVIDER_ID/scim/groups/$GROUP_ID \
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
    "id": "bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
    "displayName": "ALL EMPLOYEES",
    "externalId": "all_employees",
    "members": [
      {
        "value": "bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
        "$ref": "https://example.com/scim/v2/Users/bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
        "display": "john.smith@example.com",
        "type": "User"
      }
    ],
    "meta": {
      "created": "2025-01-01T00:00:00Z",
      "lastModified": "2025-01-02T00:00:00Z"
    },
    "schemas": [
      "urn:ietf:params:scim:schemas:core:2.0:Group"
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
    "id": "bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
    "displayName": "ALL EMPLOYEES",
    "externalId": "all_employees",
    "members": [
      {
        "value": "bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
        "$ref": "https://example.com/scim/v2/Users/bd97ef8d-7986-43e3-9ee0-c25dda33e4b0",
        "display": "john.smith@example.com",
        "type": "User"
      }
    ],
    "meta": {
      "created": "2025-01-01T00:00:00Z",
      "lastModified": "2025-01-02T00:00:00Z"
    },
    "schemas": [
      "urn:ietf:params:scim:schemas:core:2.0:Group"
    ]
  }
}
```