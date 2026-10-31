---
title: List user tenants
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[User](https://developers.cloudflare.com/api/resources/user)

[Tenants](https://developers.cloudflare.com/api/resources/user/subresources/tenants)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List user tenants

GET/user/tenants

Retrieves the legacy Tenants associated with the authenticated user. Use `GET /organizations` to list modern Organizations the user has access to.

##### Security

API Email + API Key

The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**`X-Auth-Email: user@example.com`

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**`X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194`

##### Accepted Permissions (at least one required)

`User Details Write``User Details Read`

##### ReturnsExpand Collapse

errors: array of unknown

[Link to this property](#)%20user.tenants%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

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

[Link to this property](#)%20user.tenants%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {cdate, customer\_id, edate, 10 more }

</summary>

cdate: string

formatdate-time

<a href="#">Link to this property</a>

customer\_id: string

<a href="#">Link to this property</a>

edate: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_contacts: object {email, website }

</summary>

email: optional string

<a href="#">Link to this property</a>

website: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_labels: array of string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_metadata: object {billing\_account\_type, configuration\_account, created\_by, 4 more }

</summary>

billing\_account\_type: optional string

<a href="#">Link to this property</a>

configuration\_account: optional string

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

<details>

<summary>

dns: optional object {ns\_pool }

</summary>

<details>

<summary>

ns\_pool: object {primary, secondary }

</summary>

primary: string

<a href="#">Link to this property</a>

secondary: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

flags: optional map\[string]

<a href="#">Link to this property</a>

<details>

<summary>

innate\_account\_entitlements: optional array of object {allocation, feature }

</summary>

<details>

<summary>

allocation: object {type, value }

</summary>

type: string

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {key }

</summary>

key: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_entitlements: optional array of object {allocation, feature }

</summary>

<details>

<summary>

allocation: object {type, value }

</summary>

type: string

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {key }

</summary>

key: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_name: string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_network: object {choices }

</summary>

choices: optional map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_status: string

<a href="#">Link to this property</a>

tenant\_tag: string

<a href="#">Link to this property</a>

tenant\_type: string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_units: array of object {unit\_memberships, unit\_metadata, unit\_name, 2 more }

</summary>

<details>

<summary>

unit\_memberships: array of object {member\_metadata, member\_status, member\_tag }

</summary>

member\_metadata: unknown

<a href="#">Link to this property</a>

member\_status: string

<a href="#">Link to this property</a>

member\_tag: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

unit\_metadata: unknown

<a href="#">Link to this property</a>

unit\_name: string

<a href="#">Link to this property</a>

unit\_status: string

<a href="#">Link to this property</a>

unit\_tag: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui\_flags: object {show\_orgs\_ui, show\_tenants\_ui }

Which top-level dashboard experiences to render for this tenant; both may be true.

</summary>

show\_orgs\_ui: boolean

Render the Organizations experience for this tenant.

<a href="#">Link to this property</a>

show\_tenants\_ui: boolean

Render the legacy Tenants experience for this tenant.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tenants%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20user.tenants%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List user tenants

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/user/tenants \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
```

200 example

```
{
  "errors": [],
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
  "result": [
    {
      "cdate": "2019-12-27T18:11:19.117Z",
      "customer_id": "customer_id",
      "edate": "2019-12-27T18:11:19.117Z",
      "tenant_contacts": {
        "email": "email",
        "website": "website"
      },
      "tenant_labels": [
        "string"
      ],
      "tenant_metadata": {
        "billing_account_type": "billing_account_type",
        "configuration_account": "configuration_account",
        "created_by": "created_by",
        "dns": {
          "ns_pool": {
            "primary": "primary",
            "secondary": "secondary"
          }
        },
        "flags": {
          "foo": "string"
        },
        "innate_account_entitlements": [
          {
            "allocation": {
              "type": "type",
              "value": true
            },
            "feature": {
              "key": "key"
            }
          }
        ],
        "tenant_entitlements": [
          {
            "allocation": {
              "type": "type",
              "value": true
            },
            "feature": {
              "key": "key"
            }
          }
        ]
      },
      "tenant_name": "tenant_name",
      "tenant_network": {
        "choices": {
          "foo": {}
        }
      },
      "tenant_status": "tenant_status",
      "tenant_tag": "tenant_tag",
      "tenant_type": "tenant_type",
      "tenant_units": [
        {
          "unit_memberships": [
            {
              "member_metadata": {},
              "member_status": "member_status",
              "member_tag": "member_tag"
            }
          ],
          "unit_metadata": {},
          "unit_name": "unit_name",
          "unit_status": "unit_status",
          "unit_tag": "unit_tag"
        }
      ],
      "ui_flags": {
        "show_orgs_ui": true,
        "show_tenants_ui": true
      }
    }
  ],
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [],
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
  "result": [
    {
      "cdate": "2019-12-27T18:11:19.117Z",
      "customer_id": "customer_id",
      "edate": "2019-12-27T18:11:19.117Z",
      "tenant_contacts": {
        "email": "email",
        "website": "website"
      },
      "tenant_labels": [
        "string"
      ],
      "tenant_metadata": {
        "billing_account_type": "billing_account_type",
        "configuration_account": "configuration_account",
        "created_by": "created_by",
        "dns": {
          "ns_pool": {
            "primary": "primary",
            "secondary": "secondary"
          }
        },
        "flags": {
          "foo": "string"
        },
        "innate_account_entitlements": [
          {
            "allocation": {
              "type": "type",
              "value": true
            },
            "feature": {
              "key": "key"
            }
          }
        ],
        "tenant_entitlements": [
          {
            "allocation": {
              "type": "type",
              "value": true
            },
            "feature": {
              "key": "key"
            }
          }
        ]
      },
      "tenant_name": "tenant_name",
      "tenant_network": {
        "choices": {
          "foo": {}
        }
      },
      "tenant_status": "tenant_status",
      "tenant_tag": "tenant_tag",
      "tenant_type": "tenant_type",
      "tenant_units": [
        {
          "unit_memberships": [
            {
              "member_metadata": {},
              "member_status": "member_status",
              "member_tag": "member_tag"
            }
          ],
          "unit_metadata": {},
          "unit_name": "unit_name",
          "unit_status": "unit_status",
          "unit_tag": "unit_tag"
        }
      ],
      "ui_flags": {
        "show_orgs_ui": true,
        "show_tenants_ui": true
      }
    }
  ],
  "success": true
}
```