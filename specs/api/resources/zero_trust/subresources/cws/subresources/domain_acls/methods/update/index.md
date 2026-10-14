---
title: Update a domain ACL and replace its entries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Domain ACLs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update a domain ACL and replace its entries

PUT/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

Replaces the domain access control list’s name, default action, and entries.

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

Cloudflare account ID (32-character hexadecimal string)

maxLength32

minLength32

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

domain\_acl\_id: string

ID of the domain ACL to update

formatuuid

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20domain_acl_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

default\_action: "ALLOW"or "BLOCK"

Default action when no entry matches

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20default_action%20%3E%20(schema)>)

<details>

<summary>

entries: array of object {action, domain }

Replacement set of domain entries. Each domain must appear at most once.

</summary>

<details>

<summary>

action: "ALLOW"or "BLOCK"

Per-domain decision overriding the parent ACL’s default\_action

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

domain: string

Hostname or domain pattern, capped at 255 UTF-8 bytes

maxLength255

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20entries%20%3E%20(schema)>)

name: string

Name of the domain ACL

maxLength100

minLength1

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.domain_acls%20%3E%20(model)%20domain_acl%20%3E%20(schema)">DomainACL</a> { id, created\_at, default\_action, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

default\_action: "ALLOW"or "BLOCK"

Action applied when no entry matches the request domain

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

entries: array of object {action, domain }

Per-domain action overrides. Each domain appears at most once.

</summary>

<details>

<summary>

action: "ALLOW"or "BLOCK"

Per-domain decision overriding the parent ACL’s default\_action

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

domain: string

Hostname or domain pattern, capped at 255 UTF-8 bytes

maxLength255

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Update a domain ACL and replace its entries

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/domain-acls/$DOMAIN_ACL_ID \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "default_action": "ALLOW",
          "entries": [
            {
              "action": "ALLOW",
              "domain": "x"
            }
          ],
          "name": "x"
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "default_action": "ALLOW",
    "entries": [
      {
        "action": "ALLOW",
        "domain": "x"
      }
    ],
    "name": "x",
    "updated_at": "2019-12-27T18:11:19.117Z"
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
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "default_action": "ALLOW",
    "entries": [
      {
        "action": "ALLOW",
        "domain": "x"
      }
    ],
    "name": "x",
    "updated_at": "2019-12-27T18:11:19.117Z"
  },
  "success": true
}
```