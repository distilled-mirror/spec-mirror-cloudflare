---
title: Posture
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Posture

#### PostureFindings

##### [List posture findings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/list)

GET/accounts/{account\_id}/data-security/posture/findings

##### [Get a posture finding](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/get)

GET/accounts/{account\_id}/data-security/posture/findings/{finding\_id}

##### [Create new findings export request](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/export)

POST/accounts/{account\_id}/data-security/posture/findings/export

##### [Mark a finding as ignored](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/ignore)

POST/accounts/{account\_id}/data-security/posture/findings/ignore

##### [Remove ignore marker from a finding](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/unignore)

POST/accounts/{account\_id}/data-security/posture/findings/unignore

##### [Update the severity for a finding](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/tune_severity)

POST/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/tune\_finding\_severity

##### [Reset severity for a finding back to the default](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/methods/reset_severity)

POST/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/reset\_finding\_severity

##### ModelsExpand Collapse

<details>

<summary>

FindingListResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_list_response%20%3E%20(schema)>)

<details>

<summary>

FindingGetResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_get_response%20%3E%20(schema)>)

<details>

<summary>

FindingExportResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_export_response%20%3E%20(schema)>)

<details>

<summary>

FindingIgnoreResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_ignore_response%20%3E%20(schema)>)

<details>

<summary>

FindingUnignoreResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_unignore_response%20%3E%20(schema)>)

<details>

<summary>

FindingTuneSeverityResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_tune_severity_response%20%3E%20(schema)>)

<details>

<summary>

FindingResetSeverityResponse object {id, active\_count, archived\_count, 6 more }

Aggregated finding information with counts and metadata. This is optimized for list API queries and represents a finding along with its instance statistics.

</summary>

id: string

Base64 encoded identifier of the security finding.

formatbyte

<a href="#">Link to this property</a>

active\_count: number

Number of active problematic instances identified in the security finding.

<a href="#">Link to this property</a>

archived\_count: number

Number of archived instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

finding: object {id, category, name, 15 more }

Basic finding type information.

</summary>

id: string

The unique identifier of the finding.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {observation, product, type }

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

<details>

<summary>

remediation: optional object {id, frameworks, guide, 3 more }

Remediation guide information for a finding.

</summary>

id: string

Remediation Id.

formatuuid

<a href="#">Link to this property</a>

frameworks: array of string

Relevant Compliance Frameworks.

<a href="#">Link to this property</a>

guide: string

Remediation guide text.

<a href="#">Link to this property</a>

impact: string

Description of the potential impact.

<a href="#">Link to this property</a>

locale: string

I18N Locale.

<a href="#">Link to this property</a>

threat: string

Description of the threat.

<a href="#">Link to this property</a>

</details>

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

<a href="#">Link to this property</a>

ignored: boolean

Determines if finding is currently ignored.

<a href="#">Link to this property</a>

instance\_count: number

Number of total (Active or archived) problematic instances identified in the security finding.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Timestamp of the latest affliction date of an active finding.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

severity\_override: optional object {created\_by, severity }

Override information for finding severity.

</summary>

created\_by: string

User ID who created the override.

<a href="#">Link to this property</a>

<details>

<summary>

severity: "Critical"or "High"or "Medium"or "Low"

The severity level of a finding.

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

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings%20%3E%20(model)%20finding_reset_severity_response%20%3E%20(schema)>)

#### PostureFindingsInstances

##### [List instances of a finding](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/subresources/instances/methods/list)

GET/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/instances

##### [Get a finding instance using an instance ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/subresources/instances/methods/get)

GET/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/instances/{instance\_id}

##### [Create a finding instances export](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/subresources/instances/methods/export)

POST/accounts/{account\_id}/data-security/posture/findings/{storage\_namespace\_id}/instances/export

##### [Archive a finding](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/subresources/instances/methods/archive)

POST/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/instances/archive

##### [Remove the archive marking from a finding instance](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/findings/subresources/instances/methods/unarchive)

POST/accounts/{account\_id}/data-security/posture/findings/{finding\_id}/instances/unarchive

##### ModelsExpand Collapse

<details>

<summary>

InstanceListResponse object {affliction\_date, asset, dlp\_contexts, 4 more }

A specific instance of a security finding. In the API interface, we refer to the ‘finding’ table in our DB as finding instances, optimized for the p99 use case.

</summary>

affliction\_date: string

When this specific instance was identified.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {category, external\_id, fields, 4 more }

Asset information including metadata and categorization.

</summary>

<details>

<summary>

category: object {service, type, vendor, id }

Category information for an asset.

</summary>

service: string

The specific service within the vendor the asset is part of (often none). Example - AWS is the vendor, S3 is the service.

<a href="#">Link to this property</a>

type: string

The type of asset.

<a href="#">Link to this property</a>

vendor: string

The vendor the asset is part of.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset category.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

maxLength512

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

The fields associated with the asset.

</summary>

name: string

The name of the field.

<a href="#">Link to this property</a>

value: string

The value of the field.

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

maxLength2048

<a href="#">Link to this property</a>

updated: optional string

Timestamp of the asset row version represented by this data.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

dlp\_contexts: array of object {created, entry\_ids, profile\_id, 6 more }

DLP context information if this is a content finding.

</summary>

created: string

When the DLP context was created.

formatdate-time

<a href="#">Link to this property</a>

entry\_ids: array of string

DLP Entry IDs.

<a href="#">Link to this property</a>

profile\_id: string

DLP Profile ID.

formatuuid

<a href="#">Link to this property</a>

updated: string

When the DLP context was last updated.

formatdate-time

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the DLP context.

formatuuid

<a href="#">Link to this property</a>

deleted: optional string

When the DLP context was deleted.

formatdate-time

<a href="#">Link to this property</a>

match\_context\_max\_extent: optional number

DLP Right Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_min\_extent: optional number

DLP Left Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_payload: optional map\[unknown]

DLP Match context payload that matched the profile in question.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

remediations: array of object {id, created\_at, stale, status }

A list of the 10 most recent remediation jobs for this finding instance, ordered by creation time (most recent first). The ‘stale’ field indicates whether the remediation job was created before the finding instance’s affliction\_date (true) or after it (false). If there has never been a remediation job for this finding instance, this field will be an empty array.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this remediation job is stale (created before the finding instance’s affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhooks: array of object {latest\_job, webhook\_id, webhook\_label }

The most recent webhook job invocation for each webhook configuration associated with this finding instance. Each entry represents the latest job (any status) per webhook config. The ‘stale’ field indicates whether the job was invoked before the finding instance’s current affliction\_date. If no webhook jobs have been created, this field will be an empty array.

</summary>

<details>

<summary>

latest\_job: object {id, created\_at, stale, status }

The most recent webhook job for this webhook configuration.

</summary>

id: string

Unique identifier for the webhook job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the webhook job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this webhook job is stale (created before the finding instance’s current affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"

Current status of the webhook job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

webhook\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

webhook\_label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the finding instance.

formatuuid

<a href="#">Link to this property</a>

is\_archived: optional boolean

Whether this finding instance has been archived.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings.instances%20%3E%20(model)%20instance_list_response%20%3E%20(schema)>)

<details>

<summary>

InstanceGetResponse object {affliction\_date, asset, dlp\_contexts, 4 more }

A specific instance of a security finding. In the API interface, we refer to the ‘finding’ table in our DB as finding instances, optimized for the p99 use case.

</summary>

affliction\_date: string

When this specific instance was identified.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {category, external\_id, fields, 4 more }

Asset information including metadata and categorization.

</summary>

<details>

<summary>

category: object {service, type, vendor, id }

Category information for an asset.

</summary>

service: string

The specific service within the vendor the asset is part of (often none). Example - AWS is the vendor, S3 is the service.

<a href="#">Link to this property</a>

type: string

The type of asset.

<a href="#">Link to this property</a>

vendor: string

The vendor the asset is part of.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset category.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

maxLength512

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

The fields associated with the asset.

</summary>

name: string

The name of the field.

<a href="#">Link to this property</a>

value: string

The value of the field.

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

maxLength2048

<a href="#">Link to this property</a>

updated: optional string

Timestamp of the asset row version represented by this data.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

dlp\_contexts: array of object {created, entry\_ids, profile\_id, 6 more }

DLP context information if this is a content finding.

</summary>

created: string

When the DLP context was created.

formatdate-time

<a href="#">Link to this property</a>

entry\_ids: array of string

DLP Entry IDs.

<a href="#">Link to this property</a>

profile\_id: string

DLP Profile ID.

formatuuid

<a href="#">Link to this property</a>

updated: string

When the DLP context was last updated.

formatdate-time

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the DLP context.

formatuuid

<a href="#">Link to this property</a>

deleted: optional string

When the DLP context was deleted.

formatdate-time

<a href="#">Link to this property</a>

match\_context\_max\_extent: optional number

DLP Right Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_min\_extent: optional number

DLP Left Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_payload: optional map\[unknown]

DLP Match context payload that matched the profile in question.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

remediations: array of object {id, created\_at, stale, status }

A list of the 10 most recent remediation jobs for this finding instance, ordered by creation time (most recent first). The ‘stale’ field indicates whether the remediation job was created before the finding instance’s affliction\_date (true) or after it (false). If there has never been a remediation job for this finding instance, this field will be an empty array.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this remediation job is stale (created before the finding instance’s affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhooks: array of object {latest\_job, webhook\_id, webhook\_label }

The most recent webhook job invocation for each webhook configuration associated with this finding instance. Each entry represents the latest job (any status) per webhook config. The ‘stale’ field indicates whether the job was invoked before the finding instance’s current affliction\_date. If no webhook jobs have been created, this field will be an empty array.

</summary>

<details>

<summary>

latest\_job: object {id, created\_at, stale, status }

The most recent webhook job for this webhook configuration.

</summary>

id: string

Unique identifier for the webhook job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the webhook job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this webhook job is stale (created before the finding instance’s current affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"

Current status of the webhook job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

webhook\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

webhook\_label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the finding instance.

formatuuid

<a href="#">Link to this property</a>

is\_archived: optional boolean

Whether this finding instance has been archived.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings.instances%20%3E%20(model)%20instance_get_response%20%3E%20(schema)>)

<details>

<summary>

InstanceExportResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings.instances%20%3E%20(model)%20instance_export_response%20%3E%20(schema)>)

<details>

<summary>

InstanceArchiveResponse object {affliction\_date, asset, dlp\_contexts, 4 more }

A specific instance of a security finding. In the API interface, we refer to the ‘finding’ table in our DB as finding instances, optimized for the p99 use case.

</summary>

affliction\_date: string

When this specific instance was identified.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {category, external\_id, fields, 4 more }

Asset information including metadata and categorization.

</summary>

<details>

<summary>

category: object {service, type, vendor, id }

Category information for an asset.

</summary>

service: string

The specific service within the vendor the asset is part of (often none). Example - AWS is the vendor, S3 is the service.

<a href="#">Link to this property</a>

type: string

The type of asset.

<a href="#">Link to this property</a>

vendor: string

The vendor the asset is part of.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset category.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

maxLength512

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

The fields associated with the asset.

</summary>

name: string

The name of the field.

<a href="#">Link to this property</a>

value: string

The value of the field.

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

maxLength2048

<a href="#">Link to this property</a>

updated: optional string

Timestamp of the asset row version represented by this data.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

dlp\_contexts: array of object {created, entry\_ids, profile\_id, 6 more }

DLP context information if this is a content finding.

</summary>

created: string

When the DLP context was created.

formatdate-time

<a href="#">Link to this property</a>

entry\_ids: array of string

DLP Entry IDs.

<a href="#">Link to this property</a>

profile\_id: string

DLP Profile ID.

formatuuid

<a href="#">Link to this property</a>

updated: string

When the DLP context was last updated.

formatdate-time

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the DLP context.

formatuuid

<a href="#">Link to this property</a>

deleted: optional string

When the DLP context was deleted.

formatdate-time

<a href="#">Link to this property</a>

match\_context\_max\_extent: optional number

DLP Right Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_min\_extent: optional number

DLP Left Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_payload: optional map\[unknown]

DLP Match context payload that matched the profile in question.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

remediations: array of object {id, created\_at, stale, status }

A list of the 10 most recent remediation jobs for this finding instance, ordered by creation time (most recent first). The ‘stale’ field indicates whether the remediation job was created before the finding instance’s affliction\_date (true) or after it (false). If there has never been a remediation job for this finding instance, this field will be an empty array.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this remediation job is stale (created before the finding instance’s affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhooks: array of object {latest\_job, webhook\_id, webhook\_label }

The most recent webhook job invocation for each webhook configuration associated with this finding instance. Each entry represents the latest job (any status) per webhook config. The ‘stale’ field indicates whether the job was invoked before the finding instance’s current affliction\_date. If no webhook jobs have been created, this field will be an empty array.

</summary>

<details>

<summary>

latest\_job: object {id, created\_at, stale, status }

The most recent webhook job for this webhook configuration.

</summary>

id: string

Unique identifier for the webhook job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the webhook job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this webhook job is stale (created before the finding instance’s current affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"

Current status of the webhook job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

webhook\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

webhook\_label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the finding instance.

formatuuid

<a href="#">Link to this property</a>

is\_archived: optional boolean

Whether this finding instance has been archived.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings.instances%20%3E%20(model)%20instance_archive_response%20%3E%20(schema)>)

<details>

<summary>

InstanceUnarchiveResponse object {affliction\_date, asset, dlp\_contexts, 4 more }

A specific instance of a security finding. In the API interface, we refer to the ‘finding’ table in our DB as finding instances, optimized for the p99 use case.

</summary>

affliction\_date: string

When this specific instance was identified.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {category, external\_id, fields, 4 more }

Asset information including metadata and categorization.

</summary>

<details>

<summary>

category: object {service, type, vendor, id }

Category information for an asset.

</summary>

service: string

The specific service within the vendor the asset is part of (often none). Example - AWS is the vendor, S3 is the service.

<a href="#">Link to this property</a>

type: string

The type of asset.

<a href="#">Link to this property</a>

vendor: string

The vendor the asset is part of.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset category.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

maxLength512

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

The fields associated with the asset.

</summary>

name: string

The name of the field.

<a href="#">Link to this property</a>

value: string

The value of the field.

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

maxLength2048

<a href="#">Link to this property</a>

updated: optional string

Timestamp of the asset row version represented by this data.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

dlp\_contexts: array of object {created, entry\_ids, profile\_id, 6 more }

DLP context information if this is a content finding.

</summary>

created: string

When the DLP context was created.

formatdate-time

<a href="#">Link to this property</a>

entry\_ids: array of string

DLP Entry IDs.

<a href="#">Link to this property</a>

profile\_id: string

DLP Profile ID.

formatuuid

<a href="#">Link to this property</a>

updated: string

When the DLP context was last updated.

formatdate-time

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the DLP context.

formatuuid

<a href="#">Link to this property</a>

deleted: optional string

When the DLP context was deleted.

formatdate-time

<a href="#">Link to this property</a>

match\_context\_max\_extent: optional number

DLP Right Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_min\_extent: optional number

DLP Left Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_payload: optional map\[unknown]

DLP Match context payload that matched the profile in question.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

remediations: array of object {id, created\_at, stale, status }

A list of the 10 most recent remediation jobs for this finding instance, ordered by creation time (most recent first). The ‘stale’ field indicates whether the remediation job was created before the finding instance’s affliction\_date (true) or after it (false). If there has never been a remediation job for this finding instance, this field will be an empty array.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this remediation job is stale (created before the finding instance’s affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhooks: array of object {latest\_job, webhook\_id, webhook\_label }

The most recent webhook job invocation for each webhook configuration associated with this finding instance. Each entry represents the latest job (any status) per webhook config. The ‘stale’ field indicates whether the job was invoked before the finding instance’s current affliction\_date. If no webhook jobs have been created, this field will be an empty array.

</summary>

<details>

<summary>

latest\_job: object {id, created\_at, stale, status }

The most recent webhook job for this webhook configuration.

</summary>

id: string

Unique identifier for the webhook job.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When the webhook job was created.

formatdate-time

<a href="#">Link to this property</a>

stale: boolean

Whether this webhook job is stale (created before the finding instance’s current affliction\_date).

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"

Current status of the webhook job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

webhook\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

webhook\_label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the finding instance.

formatuuid

<a href="#">Link to this property</a>

is\_archived: optional boolean

Whether this finding instance has been archived.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.findings.instances%20%3E%20(model)%20instance_unarchive_response%20%3E%20(schema)>)

#### PostureExports

##### [List all export jobs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/exports/methods/list)

GET/accounts/{account\_id}/data-security/posture/exports

##### [Get a single export job](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/exports/methods/get)

GET/accounts/{account\_id}/data-security/posture/exports/{id}

##### ModelsExpand Collapse

<details>

<summary>

ExportListResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.exports%20%3E%20(model)%20export_list_response%20%3E%20(schema)>)

<details>

<summary>

ExportGetResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.exports%20%3E%20(model)%20export_get_response%20%3E%20(schema)>)

#### PostureFinding Types

##### [List all finding types](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/list)

GET/accounts/{account\_id}/data-security/posture/finding\_types

##### [Create a custom finding type](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/create)

POST/accounts/{account\_id}/data-security/posture/finding\_types

##### [Get finding by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/get)

GET/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}

##### [Update a custom finding type](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/update)

PUT/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}

##### [Delete a custom finding type](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/delete)

DELETE/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}

##### [Validate a custom finding type](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types/methods/validate)

POST/accounts/{account\_id}/data-security/posture/finding\_types/validate

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

FindingTypeCreateResponse object {id, applies\_to\_all\_integrations, asset\_class, 14 more }

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(model)%20finding_type_create_response%20%3E%20(schema)>)

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

<details>

<summary>

FindingTypeUpdateResponse object {id, applies\_to\_all\_integrations, asset\_class, 14 more }

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(model)%20finding_type_update_response%20%3E%20(schema)>)

<details>

<summary>

FindingTypeValidateResponse object {errors, valid }

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

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(model)%20finding_type_validate_response%20%3E%20(schema)>)

#### PostureFinding TypesRemediation Types

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

#### PostureAsset Schemas

##### [List asset schemas](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/list)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas

##### [Get asset schema by asset class](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/get)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas/{asset\_class}

##### ModelsExpand Collapse

<details>

<summary>

AssetSchemaListResponse object {asset\_classes, vendor }

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

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(model)%20asset_schema_list_response%20%3E%20(schema)>)

<details>

<summary>

AssetSchemaGetResponse object {asset\_class, schema }

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicApiKey.

<a href="#">Link to this property</a>

schema: map\[unknown]

Fields and related attributes a custom finding type may reference for this asset class, as a JSON Schema. Top-level properties are <code>asset</code> and, when related resources exist, <code>associated</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(model)%20asset_schema_get_response%20%3E%20(schema)>)

#### PostureContent

##### [List DLP content findings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/content/methods/list)

GET/accounts/{account\_id}/data-security/posture/content

##### [Create a content export](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/content/methods/export)

POST/accounts/{account\_id}/data-security/posture/content/export

##### ModelsExpand Collapse

<details>

<summary>

ContentListResponse object {asset\_id, asset\_name, dlp\_contexts, 4 more }

Content asset with DLP information.

</summary>

asset\_id: string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

asset\_name: string

Name of the asset.

<a href="#">Link to this property</a>

<details>

<summary>

dlp\_contexts: array of object {created, entry\_ids, profile\_id, 6 more }

DLP context information for this asset.

</summary>

created: string

When the DLP context was created.

formatdate-time

<a href="#">Link to this property</a>

entry\_ids: array of string

DLP Entry IDs.

<a href="#">Link to this property</a>

profile\_id: string

DLP Profile ID.

formatuuid

<a href="#">Link to this property</a>

updated: string

When the DLP context was last updated.

formatdate-time

<a href="#">Link to this property</a>

id: optional string

Unique identifier for the DLP context.

formatuuid

<a href="#">Link to this property</a>

deleted: optional string

When the DLP context was deleted.

formatdate-time

<a href="#">Link to this property</a>

match\_context\_max\_extent: optional number

DLP Right Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_min\_extent: optional number

DLP Left Boundary of match context.

maximum2147483647

minimum0

<a href="#">Link to this property</a>

match\_context\_payload: optional map\[unknown]

DLP Match context payload that matched the profile in question.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

dlp\_profile\_count: number

Number of DLP profiles that flagged this asset.

<a href="#">Link to this property</a>

dlp\_profile\_ids: array of string

IDs of DLP profiles that flagged this asset.

<a href="#">Link to this property</a>

<details>

<summary>

integration: object {created, last\_hydrated, name, 12 more }

Summary information about an integration.

</summary>

created: string

When entity was created.

formatdate-time

<a href="#">Link to this property</a>

last\_hydrated: string

When were the integration credentials last updated.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the integration.

maxLength256

<a href="#">Link to this property</a>

permissions: array of string

The vendor-specific permissions associated with the integration.

<a href="#">Link to this property</a>

<details>

<summary>

policy: object {id, client\_id, compliance\_level, 4 more }

Policy configuration for an integration.

</summary>

id: optional string

Policy identifier.

formatuuid

<a href="#">Link to this property</a>

client\_id: optional string

OAuth client ID for the policy.

<a href="#">Link to this property</a>

compliance\_level: optional string

Compliance level for the policy.

<a href="#">Link to this property</a>

dlp\_enabled: optional boolean

Whether DLP is enabled for this policy.

<a href="#">Link to this property</a>

link: optional string

Link to policy documentation.

formaturi

<a href="#">Link to this property</a>

name: optional string

Policy name.

<a href="#">Link to this property</a>

permissions: optional array of string

List of permissions included in the policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: string

Current status of the integration.

<a href="#">Link to this property</a>

updated: string

Last entity was updated.

formatdate-time

<a href="#">Link to this property</a>

upgradable: boolean

Whether the integrations permissions can be updated.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: object {id, description, display\_name, 5 more }

Information about a vendor/service provider.

</summary>

id: string

The id of the vendor.

<a href="#">Link to this property</a>

description: string

Detailed information about what kinds of issues are detected for this vendor.

<a href="#">Link to this property</a>

display\_name: string

The display name of the vendor.

<a href="#">Link to this property</a>

logo: string

Logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

name: string

The name of the vendor.

<a href="#">Link to this property</a>

static\_logo: string

Static logo URL for the vendor.

formaturi

<a href="#">Link to this property</a>

zt\_enrollments: array of string

The vendor’s compatible Zero Trust products.

<a href="#">Link to this property</a>

policies: optional array of map\[unknown]

The policies related to the vendor.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

zt\_enrollments: array of object {id, description, display\_name, enabled }

Zero Trust products associated with this integration.

</summary>

id: optional string

The internal identifier of the Zero Trust Product.

<a href="#">Link to this property</a>

description: optional string

Brief description of the Zero Trust Product.

<a href="#">Link to this property</a>

display\_name: optional string

The verbose name of the Zero Trust Product.

<a href="#">Link to this property</a>

enabled: optional boolean

Flag to enable/disable access to the listed integration from the corresponding Cloudflare product.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Integration ID.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

credential\_health\_status: optional "Initializing"or "Healthy"or "Unhealthy"

Health status of integration credentials.

</summary>

One of the following:

"Initializing"

<a href="#">Link to this property</a>

"Healthy"

<a href="#">Link to this property</a>

"Unhealthy"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

credentials\_expiry: optional string

The date and time when the integration credentials will expire.

formatdate-time

<a href="#">Link to this property</a>

is\_paused: optional boolean

Whether the given integration is paused by the user.

<a href="#">Link to this property</a>

upgrade\_dismissed: optional boolean

UI State as to whether a potential permissions upgrade has been dismissed.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

latest\_affliction\_date: string

Most recent date this asset was flagged.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.content%20%3E%20(model)%20content_list_response%20%3E%20(schema)>)

<details>

<summary>

ContentExportResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.content%20%3E%20(model)%20content_export_response%20%3E%20(schema)>)

#### PostureRemediations

#### PostureRemediationsJobs

##### [List remediation jobs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/remediations/subresources/jobs/methods/list)

GET/accounts/{account\_id}/data-security/posture/remediations/jobs

##### [Creates remediation jobs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/remediations/subresources/jobs/methods/create)

POST/accounts/{account\_id}/data-security/posture/remediations/jobs

##### [Create a remediation jobs export](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/remediations/subresources/jobs/methods/export)

POST/accounts/{account\_id}/data-security/posture/remediations/jobs/export

##### ModelsExpand Collapse

<details>

<summary>

JobListResponse object {id, asset, created\_at, 11 more }

Information about a remediation job.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {id, category, external\_id, 3 more }

Asset information for a remediation job.

</summary>

id: string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {service, type, vendor }

Category information for a remediation job asset.

</summary>

service: string

Specific service within the vendor.

<a href="#">Link to this property</a>

type: string

Asset type.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: "AWS"or "Anthropic"or "Bitbucket"or 14 more

Display names for vendor types.

</summary>

One of the following:

"AWS"

<a href="#">Link to this property</a>

"Anthropic"

<a href="#">Link to this property</a>

"Bitbucket"

<a href="#">Link to this property</a>

"Box"

<a href="#">Link to this property</a>

"Confluence"

<a href="#">Link to this property</a>

"Dropbox"

<a href="#">Link to this property</a>

"GitHub"

<a href="#">Link to this property</a>

"Google Cloud Platform"

<a href="#">Link to this property</a>

"Google Workspace"

<a href="#">Link to this property</a>

"Jira"

<a href="#">Link to this property</a>

"Microsoft"

<a href="#">Link to this property</a>

"Microsoft Internal"

<a href="#">Link to this property</a>

"OpenAI"

<a href="#">Link to this property</a>

"Slack"

<a href="#">Link to this property</a>

"Salesforce"

<a href="#">Link to this property</a>

"ServiceNow"

<a href="#">Link to this property</a>

"Zoom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

Additional fields associated with the asset.

</summary>

name: string

Field name.

<a href="#">Link to this property</a>

<details>

<summary>

value: stringor numberor boolean

Field value (can be string, number, or boolean).

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

finding\_id: string

Encoded finding ID.

<a href="#">Link to this property</a>

finding\_instance\_id: string

ID of the finding instance being remediated.

formatuuid

<a href="#">Link to this property</a>

finding\_type\_id: string

ID of the finding type.

formatuuid

<a href="#">Link to this property</a>

finding\_type\_name: string

Name of the finding type.

<a href="#">Link to this property</a>

integration\_name: string

Name of the integration.

<a href="#">Link to this property</a>

last\_updated: string

When the remediation job was last updated.

formatdate-time

<a href="#">Link to this property</a>

remediation\_type: string

Type of remediation being performed.

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered\_by\_user: string

Email of the user who triggered the remediation. For account-token actors this is the literal “Account API Token”; for policy actors this is empty.

<a href="#">Link to this property</a>

<details>

<summary>

triggered\_by\_actor: optional "user"or "account\_token"

Type of actor that triggered the remediation job. Null on legacy rows created before this column was populated.

</summary>

One of the following:

"user"

<a href="#">Link to this property</a>

"account\_token"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered\_by\_id: optional string

ID of the actor that triggered the job. Meaning depends on triggered\_by\_actor. Null on legacy rows.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.remediations.jobs%20%3E%20(model)%20job_list_response%20%3E%20(schema)>)

<details>

<summary>

JobCreateResponse object {created, failed }

</summary>

<details>

<summary>

created: array of object {id, asset, created\_at, 11 more }

Successfully created remediation jobs.

</summary>

id: string

Unique identifier for the remediation job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

asset: object {id, category, external\_id, 3 more }

Asset information for a remediation job.

</summary>

id: string

Unique identifier for the asset.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

category: object {service, type, vendor }

Category information for a remediation job asset.

</summary>

service: string

Specific service within the vendor.

<a href="#">Link to this property</a>

type: string

Asset type.

<a href="#">Link to this property</a>

<details>

<summary>

vendor: "AWS"or "Anthropic"or "Bitbucket"or 14 more

Display names for vendor types.

</summary>

One of the following:

"AWS"

<a href="#">Link to this property</a>

"Anthropic"

<a href="#">Link to this property</a>

"Bitbucket"

<a href="#">Link to this property</a>

"Box"

<a href="#">Link to this property</a>

"Confluence"

<a href="#">Link to this property</a>

"Dropbox"

<a href="#">Link to this property</a>

"GitHub"

<a href="#">Link to this property</a>

"Google Cloud Platform"

<a href="#">Link to this property</a>

"Google Workspace"

<a href="#">Link to this property</a>

"Jira"

<a href="#">Link to this property</a>

"Microsoft"

<a href="#">Link to this property</a>

"Microsoft Internal"

<a href="#">Link to this property</a>

"OpenAI"

<a href="#">Link to this property</a>

"Slack"

<a href="#">Link to this property</a>

"Salesforce"

<a href="#">Link to this property</a>

"ServiceNow"

<a href="#">Link to this property</a>

"Zoom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

external\_id: string

External identifier from the source system.

<a href="#">Link to this property</a>

<details>

<summary>

fields: array of object {name, value, link }

Additional fields associated with the asset.

</summary>

name: string

Field name.

<a href="#">Link to this property</a>

<details>

<summary>

value: stringor numberor boolean

Field value (can be string, number, or boolean).

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

link: optional string

Optional link associated with the field.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name of the asset.

<a href="#">Link to this property</a>

link: optional string

Direct link to the asset.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

When the remediation job was created.

formatdate-time

<a href="#">Link to this property</a>

finding\_id: string

Encoded finding ID.

<a href="#">Link to this property</a>

finding\_instance\_id: string

ID of the finding instance being remediated.

formatuuid

<a href="#">Link to this property</a>

finding\_type\_id: string

ID of the finding type.

formatuuid

<a href="#">Link to this property</a>

finding\_type\_name: string

Name of the finding type.

<a href="#">Link to this property</a>

integration\_name: string

Name of the integration.

<a href="#">Link to this property</a>

last\_updated: string

When the remediation job was last updated.

formatdate-time

<a href="#">Link to this property</a>

remediation\_type: string

Type of remediation being performed.

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or 2 more

Status of a remediation job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"validating"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered\_by\_user: string

Email of the user who triggered the remediation. For account-token actors this is the literal “Account API Token”; for policy actors this is empty.

<a href="#">Link to this property</a>

<details>

<summary>

triggered\_by\_actor: optional "user"or "account\_token"

Type of actor that triggered the remediation job. Null on legacy rows created before this column was populated.

</summary>

One of the following:

"user"

<a href="#">Link to this property</a>

"account\_token"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered\_by\_id: optional string

ID of the actor that triggered the job. Meaning depends on triggered\_by\_actor. Null on legacy rows.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

failed: array of object {error, finding\_instance\_id }

Failed remediation job creation attempts.

</summary>

error: string

Error message describing the failure.

<a href="#">Link to this property</a>

finding\_instance\_id: string

ID of the finding instance that failed to create a remediation job.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.remediations.jobs%20%3E%20(model)%20job_create_response%20%3E%20(schema)>)

<details>

<summary>

JobExportResponse object {id, status, type, 5 more }

Information about an export job.

</summary>

id: string

Unique identifier for the export job.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "Pending"or "Success"or "Failure"or 2 more

Status of an export job.

</summary>

One of the following:

"Pending"

<a href="#">Link to this property</a>

"Success"

<a href="#">Link to this property</a>

"Failure"

<a href="#">Link to this property</a>

"Rescheduled"

<a href="#">Link to this property</a>

"In-Progress"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "finding"or "findingInstance"or "content"or "remediationJob"

Type of export job.

</summary>

One of the following:

"finding"

<a href="#">Link to this property</a>

"findingInstance"

<a href="#">Link to this property</a>

"content"

<a href="#">Link to this property</a>

"remediationJob"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_id: string

ID of the export-requesting user.

maxLength128

<a href="#">Link to this property</a>

download\_url: optional string

The URL by which the successfully created export can be downloaded by the end users.

formaturi

maxLength1024

<a href="#">Link to this property</a>

errors: optional string

Contains information on errors which may have occurred during export creation.

<a href="#">Link to this property</a>

file\_name: optional string

The base name of the file that is/was generated by the export job.

maxLength256

<a href="#">Link to this property</a>

file\_path: optional string

The full path of the file that is stored within external storage (currently R2).

maxLength512

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.remediations.jobs%20%3E%20(model)%20job_export_response%20%3E%20(schema)>)

#### PosturePolicies

##### [List policy configurations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/policies/methods/list)

GET/accounts/{account\_id}/data-security/posture/policies

##### [Create a new policy configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/policies/methods/create)

POST/accounts/{account\_id}/data-security/posture/policies

##### [Get a policy configuration by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/policies/methods/get)

GET/accounts/{account\_id}/data-security/posture/policies/{policy\_id}

##### [Update a policy configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/policies/methods/update)

PUT/accounts/{account\_id}/data-security/posture/policies/{policy\_id}

##### [Delete a policy configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/policies/methods/delete)

DELETE/accounts/{account\_id}/data-security/posture/policies/{policy\_id}

##### ModelsExpand Collapse

<details>

<summary>

PolicyListResponse object {id, actions, applies\_to\_all\_integrations, 9 more }

Response body for a policy configuration.

</summary>

id: string

Unique identifier for the policy configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

actions: object {remediation\_types, webhook\_configs }

The actions configured for this policy.

</summary>

<details>

<summary>

remediation\_types: array of object {display\_name, remediation\_type, remediation\_type\_id }

List of remediation types that will be executed.

</summary>

display\_name: string

Display name/label of the remediation type.

<a href="#">Link to this property</a>

remediation\_type: string

The system name of the remediation type.

<a href="#">Link to this property</a>

remediation\_type\_id: string

Unique identifier for the remediation type.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhook\_configs: array of object {display\_name, webhook\_config\_id }

List of webhook configurations that will be triggered.

</summary>

display\_name: string

Display name/label of the webhook configuration.

<a href="#">Link to this property</a>

webhook\_config\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: boolean

When true, the policy applies to all integrations for the account. When false, it applies only to the specified integration\_ids.

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the policy was created.

formatdate-time

<a href="#">Link to this property</a>

description: string

User-set description of what this policy does. Limited to 1000 characters.

<a href="#">Link to this property</a>

display\_name: string

Display name for the policy configuration. Limited to 255 characters.

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is enabled. Derived from disabled\_at (enabled when disabled\_at is unset).

<a href="#">Link to this property</a>

finding\_type\_id: string

The finding type this policy is associated with. Immutable after creation; attempts to change it via update are rejected.

formatuuid

<a href="#">Link to this property</a>

integration\_ids: array of string

The integrations this policy applies to.

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the policy was last updated.

formatdate-time

<a href="#">Link to this property</a>

disabled\_at: optional string

Timestamp when the policy was disabled. Omitted from the response when the policy is enabled.

formatdate-time

<a href="#">Link to this property</a>

last\_triggered\_at: optional string

Timestamp of the most recent successful policy invocation. Omitted from the response when the policy has never been successfully triggered. Only populated on GET responses; absent on responses from create/update endpoints.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.policies%20%3E%20(model)%20policy_list_response%20%3E%20(schema)>)

<details>

<summary>

PolicyCreateResponse object {id, actions, applies\_to\_all\_integrations, 9 more }

Response body for a policy configuration.

</summary>

id: string

Unique identifier for the policy configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

actions: object {remediation\_types, webhook\_configs }

The actions configured for this policy.

</summary>

<details>

<summary>

remediation\_types: array of object {display\_name, remediation\_type, remediation\_type\_id }

List of remediation types that will be executed.

</summary>

display\_name: string

Display name/label of the remediation type.

<a href="#">Link to this property</a>

remediation\_type: string

The system name of the remediation type.

<a href="#">Link to this property</a>

remediation\_type\_id: string

Unique identifier for the remediation type.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhook\_configs: array of object {display\_name, webhook\_config\_id }

List of webhook configurations that will be triggered.

</summary>

display\_name: string

Display name/label of the webhook configuration.

<a href="#">Link to this property</a>

webhook\_config\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: boolean

When true, the policy applies to all integrations for the account. When false, it applies only to the specified integration\_ids.

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the policy was created.

formatdate-time

<a href="#">Link to this property</a>

description: string

User-set description of what this policy does. Limited to 1000 characters.

<a href="#">Link to this property</a>

display\_name: string

Display name for the policy configuration. Limited to 255 characters.

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is enabled. Derived from disabled\_at (enabled when disabled\_at is unset).

<a href="#">Link to this property</a>

finding\_type\_id: string

The finding type this policy is associated with. Immutable after creation; attempts to change it via update are rejected.

formatuuid

<a href="#">Link to this property</a>

integration\_ids: array of string

The integrations this policy applies to.

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the policy was last updated.

formatdate-time

<a href="#">Link to this property</a>

disabled\_at: optional string

Timestamp when the policy was disabled. Omitted from the response when the policy is enabled.

formatdate-time

<a href="#">Link to this property</a>

last\_triggered\_at: optional string

Timestamp of the most recent successful policy invocation. Omitted from the response when the policy has never been successfully triggered. Only populated on GET responses; absent on responses from create/update endpoints.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.policies%20%3E%20(model)%20policy_create_response%20%3E%20(schema)>)

<details>

<summary>

PolicyGetResponse object {id, actions, applies\_to\_all\_integrations, 9 more }

Response body for a policy configuration.

</summary>

id: string

Unique identifier for the policy configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

actions: object {remediation\_types, webhook\_configs }

The actions configured for this policy.

</summary>

<details>

<summary>

remediation\_types: array of object {display\_name, remediation\_type, remediation\_type\_id }

List of remediation types that will be executed.

</summary>

display\_name: string

Display name/label of the remediation type.

<a href="#">Link to this property</a>

remediation\_type: string

The system name of the remediation type.

<a href="#">Link to this property</a>

remediation\_type\_id: string

Unique identifier for the remediation type.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhook\_configs: array of object {display\_name, webhook\_config\_id }

List of webhook configurations that will be triggered.

</summary>

display\_name: string

Display name/label of the webhook configuration.

<a href="#">Link to this property</a>

webhook\_config\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: boolean

When true, the policy applies to all integrations for the account. When false, it applies only to the specified integration\_ids.

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the policy was created.

formatdate-time

<a href="#">Link to this property</a>

description: string

User-set description of what this policy does. Limited to 1000 characters.

<a href="#">Link to this property</a>

display\_name: string

Display name for the policy configuration. Limited to 255 characters.

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is enabled. Derived from disabled\_at (enabled when disabled\_at is unset).

<a href="#">Link to this property</a>

finding\_type\_id: string

The finding type this policy is associated with. Immutable after creation; attempts to change it via update are rejected.

formatuuid

<a href="#">Link to this property</a>

integration\_ids: array of string

The integrations this policy applies to.

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the policy was last updated.

formatdate-time

<a href="#">Link to this property</a>

disabled\_at: optional string

Timestamp when the policy was disabled. Omitted from the response when the policy is enabled.

formatdate-time

<a href="#">Link to this property</a>

last\_triggered\_at: optional string

Timestamp of the most recent successful policy invocation. Omitted from the response when the policy has never been successfully triggered. Only populated on GET responses; absent on responses from create/update endpoints.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.policies%20%3E%20(model)%20policy_get_response%20%3E%20(schema)>)

<details>

<summary>

PolicyUpdateResponse object {id, actions, applies\_to\_all\_integrations, 9 more }

Response body for a policy configuration.

</summary>

id: string

Unique identifier for the policy configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

actions: object {remediation\_types, webhook\_configs }

The actions configured for this policy.

</summary>

<details>

<summary>

remediation\_types: array of object {display\_name, remediation\_type, remediation\_type\_id }

List of remediation types that will be executed.

</summary>

display\_name: string

Display name/label of the remediation type.

<a href="#">Link to this property</a>

remediation\_type: string

The system name of the remediation type.

<a href="#">Link to this property</a>

remediation\_type\_id: string

Unique identifier for the remediation type.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

webhook\_configs: array of object {display\_name, webhook\_config\_id }

List of webhook configurations that will be triggered.

</summary>

display\_name: string

Display name/label of the webhook configuration.

<a href="#">Link to this property</a>

webhook\_config\_id: string

Unique identifier for the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

applies\_to\_all\_integrations: boolean

When true, the policy applies to all integrations for the account. When false, it applies only to the specified integration\_ids.

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the policy was created.

formatdate-time

<a href="#">Link to this property</a>

description: string

User-set description of what this policy does. Limited to 1000 characters.

<a href="#">Link to this property</a>

display\_name: string

Display name for the policy configuration. Limited to 255 characters.

<a href="#">Link to this property</a>

enabled: boolean

Whether the policy is enabled. Derived from disabled\_at (enabled when disabled\_at is unset).

<a href="#">Link to this property</a>

finding\_type\_id: string

The finding type this policy is associated with. Immutable after creation; attempts to change it via update are rejected.

formatuuid

<a href="#">Link to this property</a>

integration\_ids: array of string

The integrations this policy applies to.

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the policy was last updated.

formatdate-time

<a href="#">Link to this property</a>

disabled\_at: optional string

Timestamp when the policy was disabled. Omitted from the response when the policy is enabled.

formatdate-time

<a href="#">Link to this property</a>

last\_triggered\_at: optional string

Timestamp of the most recent successful policy invocation. Omitted from the response when the policy has never been successfully triggered. Only populated on GET responses; absent on responses from create/update endpoints.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.policies%20%3E%20(model)%20policy_update_response%20%3E%20(schema)>)

<details>

<summary>

PolicyDeleteResponse object {id }

Response from DeletePolicy operation.

</summary>

id: string

ID of the policy deleted.

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.policies%20%3E%20(model)%20policy_delete_response%20%3E%20(schema)>)

#### PostureWebhooks

##### [List webhook configurations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/list)

GET/accounts/{account\_id}/data-security/posture/webhooks

##### [Create a new webhook configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/create)

POST/accounts/{account\_id}/data-security/posture/webhooks

##### [Get webhook configuration by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/get)

GET/accounts/{account\_id}/data-security/posture/webhooks/{webhook\_id}

##### [Update an existing webhook configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/update)

PUT/accounts/{account\_id}/data-security/posture/webhooks/{webhook\_id}

##### [Delete a webhook configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/delete)

DELETE/accounts/{account\_id}/data-security/posture/webhooks/{webhook\_id}

##### [Test a webhook configuration before creating it](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/evaluate)

POST/accounts/{account\_id}/data-security/posture/webhooks/evaluate

##### [Test an existing webhook configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/methods/evaluate_existing)

POST/accounts/{account\_id}/data-security/posture/webhooks/{webhook\_id}/evaluate

##### ModelsExpand Collapse

<details>

<summary>

WebhookListResponse object {id, authentication\_type, created\_at, 6 more }

Webhook configuration for sending finding notifications.

</summary>

id: string

Unique identifier for the specific webhook configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_type: "Basic Auth"or "None"or "Bearer Auth"or 2 more

Type of authentication used for the webhook.

</summary>

One of the following:

"Basic Auth"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

"Bearer Auth"

<a href="#">Link to this property</a>

"Static Headers"

<a href="#">Link to this property</a>

"HMAC-Signing"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the webhook configuration was created.

formatdate-time

<a href="#">Link to this property</a>

destination\_url: string

Target URL for the webhook configuration. Where resulting data will be sent.

formaturi

<a href="#">Link to this property</a>

label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

<details>

<summary>

status: "enabled"or "disabled"

Current status of the webhook configuration. If disabled, data cannot be sent through this configuration.

</summary>

One of the following:

"enabled"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the webhook configuration was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: number

Version number of the configuration.

formatuint32

<a href="#">Link to this property</a>

<details>

<summary>

headers: optional array of object {key, value }

List of header keys configured for this webhook. Values are not included for security reasons.

</summary>

key: optional string

Header key name (lowercase).

<a href="#">Link to this property</a>

value: optional string

Header value. This field is never returned in API responses for security reasons.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_list_response%20%3E%20(schema)>)

<details>

<summary>

WebhookCreateResponse object {id, authentication\_type, created\_at, 6 more }

Webhook configuration for sending finding notifications.

</summary>

id: string

Unique identifier for the specific webhook configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_type: "Basic Auth"or "None"or "Bearer Auth"or 2 more

Type of authentication used for the webhook.

</summary>

One of the following:

"Basic Auth"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

"Bearer Auth"

<a href="#">Link to this property</a>

"Static Headers"

<a href="#">Link to this property</a>

"HMAC-Signing"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the webhook configuration was created.

formatdate-time

<a href="#">Link to this property</a>

destination\_url: string

Target URL for the webhook configuration. Where resulting data will be sent.

formaturi

<a href="#">Link to this property</a>

label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

<details>

<summary>

status: "enabled"or "disabled"

Current status of the webhook configuration. If disabled, data cannot be sent through this configuration.

</summary>

One of the following:

"enabled"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the webhook configuration was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: number

Version number of the configuration.

formatuint32

<a href="#">Link to this property</a>

<details>

<summary>

headers: optional array of object {key, value }

List of header keys configured for this webhook. Values are not included for security reasons.

</summary>

key: optional string

Header key name (lowercase).

<a href="#">Link to this property</a>

value: optional string

Header value. This field is never returned in API responses for security reasons.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_create_response%20%3E%20(schema)>)

<details>

<summary>

WebhookGetResponse object {id, authentication\_type, created\_at, 6 more }

Webhook configuration for sending finding notifications.

</summary>

id: string

Unique identifier for the specific webhook configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_type: "Basic Auth"or "None"or "Bearer Auth"or 2 more

Type of authentication used for the webhook.

</summary>

One of the following:

"Basic Auth"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

"Bearer Auth"

<a href="#">Link to this property</a>

"Static Headers"

<a href="#">Link to this property</a>

"HMAC-Signing"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the webhook configuration was created.

formatdate-time

<a href="#">Link to this property</a>

destination\_url: string

Target URL for the webhook configuration. Where resulting data will be sent.

formaturi

<a href="#">Link to this property</a>

label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

<details>

<summary>

status: "enabled"or "disabled"

Current status of the webhook configuration. If disabled, data cannot be sent through this configuration.

</summary>

One of the following:

"enabled"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the webhook configuration was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: number

Version number of the configuration.

formatuint32

<a href="#">Link to this property</a>

<details>

<summary>

headers: optional array of object {key, value }

List of header keys configured for this webhook. Values are not included for security reasons.

</summary>

key: optional string

Header key name (lowercase).

<a href="#">Link to this property</a>

value: optional string

Header value. This field is never returned in API responses for security reasons.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_get_response%20%3E%20(schema)>)

<details>

<summary>

WebhookUpdateResponse object {id, authentication\_type, created\_at, 6 more }

Webhook configuration for sending finding notifications.

</summary>

id: string

Unique identifier for the specific webhook configuration.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_type: "Basic Auth"or "None"or "Bearer Auth"or 2 more

Type of authentication used for the webhook.

</summary>

One of the following:

"Basic Auth"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

"Bearer Auth"

<a href="#">Link to this property</a>

"Static Headers"

<a href="#">Link to this property</a>

"HMAC-Signing"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp when the webhook configuration was created.

formatdate-time

<a href="#">Link to this property</a>

destination\_url: string

Target URL for the webhook configuration. Where resulting data will be sent.

formaturi

<a href="#">Link to this property</a>

label: string

Account-specified display label for the webhook configuration.

<a href="#">Link to this property</a>

<details>

<summary>

status: "enabled"or "disabled"

Current status of the webhook configuration. If disabled, data cannot be sent through this configuration.

</summary>

One of the following:

"enabled"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the webhook configuration was last updated.

formatdate-time

<a href="#">Link to this property</a>

version: number

Version number of the configuration.

formatuint32

<a href="#">Link to this property</a>

<details>

<summary>

headers: optional array of object {key, value }

List of header keys configured for this webhook. Values are not included for security reasons.

</summary>

key: optional string

Header key name (lowercase).

<a href="#">Link to this property</a>

value: optional string

Header value. This field is never returned in API responses for security reasons.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_update_response%20%3E%20(schema)>)

<details>

<summary>

WebhookDeleteResponse object {errors, messages, success }

Common response structure for all API endpoints.

</summary>

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

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: boolean

Whether the API call was successful.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_delete_response%20%3E%20(schema)>)

<details>

<summary>

WebhookEvaluateResponse object {message, status\_code, success }

Response body for webhook evaluation test results.

</summary>

message: string

Human-readable message describing the test result.

<a href="#">Link to this property</a>

status\_code: number

HTTP status code returned by the webhook endpoint. 0 if connection failed.

<a href="#">Link to this property</a>

success: boolean

Whether the webhook test was successful (received 2xx response).

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_evaluate_response%20%3E%20(schema)>)

<details>

<summary>

WebhookEvaluateExistingResponse object {message, status\_code, success }

Response body for webhook evaluation test results.

</summary>

message: string

Human-readable message describing the test result.

<a href="#">Link to this property</a>

status\_code: number

HTTP status code returned by the webhook endpoint. 0 if connection failed.

<a href="#">Link to this property</a>

success: boolean

Whether the webhook test was successful (received 2xx response).

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks%20%3E%20(model)%20webhook_evaluate_existing_response%20%3E%20(schema)>)

#### PostureWebhooksJobs

##### [Create webhook jobs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/webhooks/subresources/jobs/methods/create)

POST/accounts/{account\_id}/data-security/posture/webhooks/jobs

##### ModelsExpand Collapse

<details>

<summary>

JobCreateResponse object {created, failed }

</summary>

<details>

<summary>

created: array of object {id, asset\_data, created\_at, 9 more }

Successfully created webhook jobs.

</summary>

id: string

Unique identifier for the webhook job.

formatuuid

<a href="#">Link to this property</a>

asset\_data: map\[unknown]

Asset data associated with this webhook job.

<a href="#">Link to this property</a>

created\_at: string

When the webhook job was created.

formatdate-time

<a href="#">Link to this property</a>

integration\_id: string

ID of the integration.

formatuuid

<a href="#">Link to this property</a>

last\_updated\_at: string

When the webhook job was last updated.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

parameters: object {finding\_instance\_id }

Parameters for a webhook job.

</summary>

finding\_instance\_id: string

ID of the finding instance.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "processing"or "completed"or "failed"

Status of a webhook job.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"processing"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

triggered\_by\_actor: "user"or "account\_token"

Type of actor that triggered the webhook job.

</summary>

One of the following:

"user"

<a href="#">Link to this property</a>

"account\_token"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered\_by\_id: string

ID of the actor that triggered the job.

<a href="#">Link to this property</a>

webhook\_id: string

ID of the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

failure\_details: optional map\[unknown]

Additional details about the failure.

<a href="#">Link to this property</a>

<details>

<summary>

failure\_reason: optional "Permission Denied"or "Integration Unavailable"or "Service Temporarily Unavailable"or "System Error"

Reason for webhook job failure.

</summary>

One of the following:

"Permission Denied"

<a href="#">Link to this property</a>

"Integration Unavailable"

<a href="#">Link to this property</a>

"Service Temporarily Unavailable"

<a href="#">Link to this property</a>

"System Error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

failed: array of object {error, finding\_instance\_id, webhook\_id }

Failed webhook job creation attempts.

</summary>

error: string

Error message describing the failure.

<a href="#">Link to this property</a>

finding\_instance\_id: string

ID of the finding instance that failed to create a webhook job.

formatuuid

<a href="#">Link to this property</a>

webhook\_id: string

ID of the webhook configuration.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.webhooks.jobs%20%3E%20(model)%20job_create_response%20%3E%20(schema)>)