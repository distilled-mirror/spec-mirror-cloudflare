---
title: Create a custom finding type
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

[Finding Types](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create a custom finding type

POST/accounts/{account\_id}/data-security/posture/finding\_types

Create a new custom finding type with policy definition.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

applies\_to\_all\_integrations: boolean

When true, this finding type applies to every current and future integration of the vendor.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20applies_to_all_integrations%20%3E%20(schema)>)

asset\_class: string

Asset class this finding type applies to (PascalCase, e.g. GoogleWorkspaceFile)

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20asset_class%20%3E%20(schema)>)

<details>

<summary>

asset\_vendor: "ANTHROPIC"or "AWS"or "BITBUCKET"or 13 more

Canonical vendor enum for the platform whose assets this finding type evaluates.

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

"ZOOM"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20asset_vendor%20%3E%20(schema)>)

description: string

Human-readable description of the finding type. Cannot be empty. Maximum 4096 characters.

maxLength4096

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20description%20%3E%20(schema)>)

expression: string

Rego expression body for the policy. `package cloudflare.casb.custom` and `import rego.v1` are added automatically. Do not include package or import declarations. This field cannot be changed after creation. Maximum 4096 characters.

maxLength4096

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20expression%20%3E%20(schema)>)

name: string

Human-readable name for the finding type. Maximum 256 characters.

maxLength256

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

Default severity used when no integration-specific severity override exists.

</summary>

One of the following:

"Critical"

<a href="#">Link to this property</a>

"High"

<a href="#">Link to this property</a>

"Medium"

<a href="#">Link to this property</a>

"Low"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20severity%20%3E%20(schema)>)

integration\_ids: optional array of string

Required and non-empty when applies\_to\_all\_integrations is false; omit when it is true.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20integration_ids%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {id, applies\_to\_all\_integrations, asset\_class, 14 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: boolean

Whether this finding type applies to every current and future integration of the vendor.

<a href="#">Link to this property</a>

asset\_class: string

Asset class the finding type’s policy evaluates.

<a href="#">Link to this property</a>

<details>

<summary>

asset\_vendor: "ANTHROPIC"or "AWS"or "BITBUCKET"or 13 more

Canonical vendor enum value.

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

"ZOOM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

Category information for a finding.

</summary>

<details>

<summary>

observation: "Issue"or "Insight"or "Activity"

The type of the observation.

</summary>

One of the following:

"Issue"

<a href="#">Link to this property</a>

"Insight"

<a href="#">Link to this property</a>

"Activity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

product: "SaaS"or "Cloud"

The product category.

</summary>

One of the following:

"SaaS"

<a href="#">Link to this property</a>

"Cloud"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "Content"or "Posture"

The type of the finding category.

</summary>

One of the following:

"Content"

<a href="#">Link to this property</a>

"Posture"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the finding type was created.

formatdate-time

<a href="#">Link to this property</a>

description: string

Detailed description of the finding.

<a href="#">Link to this property</a>

expression: string

Rego expression backing this finding type. For custom finding types, generated package and import declarations are omitted. System expressions are returned unchanged.

<a href="#">Link to this property</a>

name: string

The name of the finding.

<a href="#">Link to this property</a>

<details>

<summary>

origin: "system"or "custom"

Whether the finding type is system-managed or customer-created.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

Default severity used when no integration-specific severity override exists.

</summary>

One of the following:

"Critical"

<a href="#">Link to this property</a>

"High"

<a href="#">Link to this property</a>

"Medium"

<a href="#">Link to this property</a>

"Low"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the finding type was last updated.

formatdate-time

<a href="#">Link to this property</a>

vendor: string

The SaaS/Cloud vendor of the platform with which the finding is associated.

<a href="#">Link to this property</a>

version: number

Current version of the finding type. Incremented on each update.

formatuint32

<a href="#">Link to this property</a>

integration\_ids: optional array of string

Integrations this finding type applies to when applies\_to\_all\_integrations is false.

<a href="#">Link to this property</a>

match\_count: optional number

Number of currently active finding instances across the account’s integrations. Zero when none have been detected.

formatint64

<a href="#">Link to this property</a>

quarantined: optional boolean

Whether evaluation of this finding type is suspended by an operator. Present only when true.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Create a custom finding type

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/data-security/posture/finding_types \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "applies_to_all_integrations": true,
          "asset_class": "GoogleWorkspaceFile",
          "asset_vendor": "GOOGLE_WORKSPACE",
          "description": "Detects files shared with too many users",
          "expression": "result := \\"pass\\"",
          "name": "Excessive File Sharing",
          "severity": "High",
          "integration_ids": [
            "550e8400-e29b-41d4-a716-446655440000"
          ]
        }'
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
  "result": {
    "id": "a20895dd-9c3b-43bd-a608-71c98c6c2d94",
    "applies_to_all_integrations": true,
    "asset_class": "GoogleWorkspaceFile",
    "asset_vendor": "GOOGLE_WORKSPACE",
    "category": {
      "observation": "Issue",
      "product": "SaaS",
      "type": "Posture"
    },
    "created_at": "2024-01-15T10:30:00Z",
    "description": "This finding indicates that a file in your Slack workspace is publicly accessible.",
    "expression": "expression",
    "name": "Slack File Publicly Accessible",
    "origin": "system",
    "severity": "High",
    "updated_at": "2024-01-15T10:30:00Z",
    "vendor": "Google Workspace",
    "version": 0,
    "integration_ids": [
      "550e8400-e29b-41d4-a716-446655440000"
    ],
    "match_count": 142,
    "quarantined": true
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
  "result": {
    "id": "a20895dd-9c3b-43bd-a608-71c98c6c2d94",
    "applies_to_all_integrations": true,
    "asset_class": "GoogleWorkspaceFile",
    "asset_vendor": "GOOGLE_WORKSPACE",
    "category": {
      "observation": "Issue",
      "product": "SaaS",
      "type": "Posture"
    },
    "created_at": "2024-01-15T10:30:00Z",
    "description": "This finding indicates that a file in your Slack workspace is publicly accessible.",
    "expression": "expression",
    "name": "Slack File Publicly Accessible",
    "origin": "system",
    "severity": "High",
    "updated_at": "2024-01-15T10:30:00Z",
    "vendor": "Google Workspace",
    "version": 0,
    "integration_ids": [
      "550e8400-e29b-41d4-a716-446655440000"
    ],
    "match_count": 142,
    "quarantined": true
  }
}
```