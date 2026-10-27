---
title: Validate a custom finding type
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

# Validate a custom finding type

POST/accounts/{account\_id}/data-security/posture/finding\_types/validate

Check a candidate custom finding type without creating it, so problems can be corrected before publishing. The request body is the same shape as `CreateFindingType`, and the candidate is checked against the same rules, so a valid result means the definition itself is sound. It is not a reservation: a create can still be rejected for a reason that does not belong to the definition, such as the account already holding the maximum number of custom finding types.

A candidate that fails validation is still a **200** with `result.valid: false` and one entry in `result.errors` per problem — that is the answer this endpoint exists to give. `4xx` is reserved for a request that could not be processed at all, such as a body that will not parse.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

applies\_to\_all\_integrations: boolean

When true, this finding type applies to every current and future integration of the vendor.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20applies_to_all_integrations%20%3E%20(schema)>)

asset\_class: string

Asset class this finding type applies to (PascalCase, e.g. GoogleWorkspaceFile)

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20asset_class%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20asset_vendor%20%3E%20(schema)>)

description: string

Human-readable description of the finding type. Cannot be empty. Maximum 4096 characters.

maxLength4096

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20description%20%3E%20(schema)>)

expression: string

Rego expression body for the policy. `package cloudflare.casb.custom` and `import rego.v1` are added automatically. Do not include package or import declarations. This field cannot be changed after creation. Maximum 4096 characters.

maxLength4096

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20expression%20%3E%20(schema)>)

name: string

Human-readable name for the finding type. Maximum 256 characters.

maxLength256

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20severity%20%3E%20(schema)>)

integration\_ids: optional array of string

Required and non-empty when applies\_to\_all\_integrations is false; omit when it is true.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(params)%200%20%3E%20(param)%20integration_ids%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {errors, valid }

</summary>

<details>

<summary>

errors: array of object {detail, message, code, 3 more }

Every problem found with the candidate, so all of them can be surfaced at once. Empty when <code>valid</code> is true. Problems without a location come first, followed by located problems ordered by <code>line</code>, then <code>column</code>.

</summary>

detail: string

Description of the problem.

<a href="#">Link to this property</a>

Deprecatedmessage: string

Deprecated: use <code>detail</code>.

<a href="#">Link to this property</a>

code: optional string

Machine-readable identifier for the class of problem, when one is available. Omitted otherwise.

<a href="#">Link to this property</a>

column: optional number

1-based column on <code>line</code>. Omitted when the problem could not be located in the submitted source.

<a href="#">Link to this property</a>

field: optional string

Request field the problem belongs to, matching the property names of <code>ValidateFindingTypeRequest</code>. Array properties are reported per entry with a zero-based index, for example <code>integration_ids[0]</code>. Empty when the problem cannot be attributed to a single submitted field.

<a href="#">Link to this property</a>

line: optional number

1-based line in <code>expression</code> where the problem was found. Omitted when the problem could not be located in the submitted source.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

valid: boolean

Whether the candidate finding type would be accepted as-is.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20validate%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Validate a custom finding type

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/data-security/posture/finding_types/validate \
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
    "errors": [
      {
        "detail": "\"result\" must be the string \"pass\" or \"fail\"",
        "message": "REGO_COMPILE_ERROR: undefined ref: input.asset.definitely_not_a_field (line 3, col 14)",
        "code": "REGO_COMPILE_ERROR",
        "column": 14,
        "field": "expression",
        "line": 3
      }
    ],
    "valid": true
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
    "errors": [
      {
        "detail": "\"result\" must be the string \"pass\" or \"fail\"",
        "message": "REGO_COMPILE_ERROR: undefined ref: input.asset.definitely_not_a_field (line 3, col 14)",
        "code": "REGO_COMPILE_ERROR",
        "column": 14,
        "field": "expression",
        "line": 3
      }
    ],
    "valid": true
  }
}
```