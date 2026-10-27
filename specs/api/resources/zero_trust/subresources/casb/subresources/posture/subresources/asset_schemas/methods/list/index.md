---
title: List asset schemas
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

[Asset Schemas](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List asset schemas

GET/accounts/{account\_id}/data-security/posture/asset\_schemas

Returns the catalog of asset classes available when authoring custom findings, grouped by vendor. Optionally filter to a single vendor with the `vendor` query parameter.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Zero Trust Read``Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

vendor: optional "ANTHROPIC"or "AWS"or "BITBUCKET"or 14 more

Restrict the result to a single vendor. Unknown values return 400.

</summary>

One of the following:

"ANTHROPIC"

<a href="#">Link to this property</a>

"AWS"

<a href="#">Link to this property</a>

"BITBUCKET"

<a href="#">Link to this property</a>

"BOX"

<a href="#">Link to this property</a>

"CONFLUENCE"

<a href="#">Link to this property</a>

"DROPBOX"

<a href="#">Link to this property</a>

"GITHUB"

<a href="#">Link to this property</a>

"GOOGLE\_CLOUD\_PLATFORM"

<a href="#">Link to this property</a>

"GOOGLE\_WORKSPACE"

<a href="#">Link to this property</a>

"JIRA"

<a href="#">Link to this property</a>

"MICROSOFT"

<a href="#">Link to this property</a>

"OPENAI"

<a href="#">Link to this property</a>

"SALESFORCE"

<a href="#">Link to this property</a>

"SERVICENOW"

<a href="#">Link to this property</a>

"SLACK"

<a href="#">Link to this property</a>

"WORKDAY"

<a href="#">Link to this property</a>

"ZOOM"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20vendor%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

Error or message code.

minimum1000

<a href="#">Link to this property</a>

message: string

Human-readable message.

<a href="#">Link to this property</a>

documentation\_url: optional string

Link to relevant documentation.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

JSON pointer to the source of the error.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

Error or message code.

minimum1000

<a href="#">Link to this property</a>

message: string

Human-readable message.

<a href="#">Link to this property</a>

documentation\_url: optional string

Link to relevant documentation.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

JSON pointer to the source of the error.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional array of object {asset\_classes, vendor }

Asset classes grouped by vendor, sorted by vendor enum.

</summary>

<details>

<summary>

asset\_classes: array of object {asset\_class }

Asset classes belonging to this vendor, sorted by asset\_class.

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicUser.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

vendor: string

Canonical vendor enum value, e.g. GOOGLE\_WORKSPACE.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### List asset schemas

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/data-security/posture/asset_schemas \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "success": true,
  "result": [
    {
      "asset_classes": [
        {
          "asset_class": "AnthropicApiKey"
        },
        {
          "asset_class": "AnthropicUser"
        },
        {
          "asset_class": "AnthropicWorkspace"
        }
      ],
      "vendor": "ANTHROPIC"
    },
    {
      "asset_classes": [
        {
          "asset_class": "GitHubOrganization"
        },
        {
          "asset_class": "GitHubRepository"
        },
        {
          "asset_class": "GitHubUser"
        }
      ],
      "vendor": "GITHUB"
    }
  ]
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "success": true,
  "result": [
    {
      "asset_classes": [
        {
          "asset_class": "AnthropicApiKey"
        },
        {
          "asset_class": "AnthropicUser"
        },
        {
          "asset_class": "AnthropicWorkspace"
        }
      ],
      "vendor": "ANTHROPIC"
    },
    {
      "asset_classes": [
        {
          "asset_class": "GitHubOrganization"
        },
        {
          "asset_class": "GitHubRepository"
        },
        {
          "asset_class": "GitHubUser"
        }
      ],
      "vendor": "GITHUB"
    }
  ]
}
```