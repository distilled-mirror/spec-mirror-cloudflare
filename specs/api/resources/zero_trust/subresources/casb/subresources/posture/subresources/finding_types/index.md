---
title: Finding Types
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Finding Types

##### [List all finding types](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/list)

GET/accounts/{account\_id}/data-security/posture/finding\_types

##### [Get finding by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/get)

GET/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}

##### ModelsExpand Collapse

<details>

<summary>

FindingTypeListResponse object {id, category, name, 14 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

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

name: string

The name of the finding.

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

vendor: string

The SaaS/Cloud vendor of the platform with which the finding is associated.

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: optional boolean

Whether this finding type applies to every current and future integration of the vendor.

<a href="#">Link to this property</a>

asset\_class: optional string

Asset class the finding type’s policy evaluates.

<a href="#">Link to this property</a>

<details>

<summary>

asset\_vendor: optional "ANTHROPIC"or "AWS"or "BITBUCKET"or 13 more

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

created\_at: optional string

Timestamp when the finding type was created.

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Detailed description of the finding.

<a href="#">Link to this property</a>

expression: optional string

Rego expression backing this finding type. For custom finding types, generated package and import declarations are omitted. System expressions are returned unchanged.

<a href="#">Link to this property</a>

integration\_ids: optional array of string

Integrations this finding type applies to when applies\_to\_all\_integrations is false.

<a href="#">Link to this property</a>

match\_count: optional number

Number of currently active finding instances across the account’s integrations. Zero when none have been detected.

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

origin: optional "system"or "custom"

Whether the finding type is system-managed or customer-created.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

quarantined: optional boolean

Whether evaluation of this finding type is suspended by an operator. Present only when true.

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp when the finding type was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: optional number

Current version of the finding type. Incremented on each update.

formatuint32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(model)%20finding_type_list_response%20%3E%20(schema)>)

<details>

<summary>

FindingTypeGetResponse object {id, category, name, 14 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

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

name: string

The name of the finding.

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

vendor: string

The SaaS/Cloud vendor of the platform with which the finding is associated.

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: optional boolean

Whether this finding type applies to every current and future integration of the vendor.

<a href="#">Link to this property</a>

asset\_class: optional string

Asset class the finding type’s policy evaluates.

<a href="#">Link to this property</a>

<details>

<summary>

asset\_vendor: optional "ANTHROPIC"or "AWS"or "BITBUCKET"or 13 more

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

created\_at: optional string

Timestamp when the finding type was created.

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Detailed description of the finding.

<a href="#">Link to this property</a>

expression: optional string

Rego expression backing this finding type. For custom finding types, generated package and import declarations are omitted. System expressions are returned unchanged.

<a href="#">Link to this property</a>

integration\_ids: optional array of string

Integrations this finding type applies to when applies\_to\_all\_integrations is false.

<a href="#">Link to this property</a>

match\_count: optional number

Number of currently active finding instances across the account’s integrations. Zero when none have been detected.

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

origin: optional "system"or "custom"

Whether the finding type is system-managed or customer-created.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

quarantined: optional boolean

Whether evaluation of this finding type is suspended by an operator. Present only when true.

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp when the finding type was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: optional number

Current version of the finding type. Incremented on each update.

formatuint32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(model)%20finding_type_get_response%20%3E%20(schema)>)

#### Finding TypesRemediation Types

##### [List remediation types for a finding type](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/subresources/remediation_types/methods/list)

GET/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}/remediation\_types

##### ModelsExpand Collapse

<details>

<summary>

RemediationTypeListResponse object {id, description, display\_name, 2 more }

Information about a remediation type.

</summary>

id: string

The identifier for the remediation type.

formatuuid

<a href="#">Link to this property</a>

description: string

A description of the action(s) taken by the remediation type.

<a href="#">Link to this property</a>

display\_name: string

The name of the remediation type as displayed in the cloudflare dashboard.

<a href="#">Link to this property</a>

finding\_type\_id: string

The identifier of the finding\_type which this remediation type should remediate.

formatuuid

<a href="#">Link to this property</a>

remediation\_type: string

The name of the remediation type.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.finding_types.remediation_types%20%3E%20(model)%20remediation_type_list_response%20%3E%20(schema)>)