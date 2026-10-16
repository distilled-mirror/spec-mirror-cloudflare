##### [List custom prompt topics](/api/resources/zero_trust/subresources/dlp/subresources/custom_prompt_topics/methods/list)

GET/accounts/{account_id}/dlp/custom_prompt_topics

##### [Get custom prompt topic](/api/resources/zero_trust/subresources/dlp/subresources/custom_prompt_topics/methods/get)

GET/accounts/{account_id}/dlp/custom_prompt_topics/{entry_id}

##### [Create custom prompt topic](/api/resources/zero_trust/subresources/dlp/subresources/custom_prompt_topics/methods/create)

POST/accounts/{account_id}/dlp/custom_prompt_topics

##### [Update custom prompt topic](/api/resources/zero_trust/subresources/dlp/subresources/custom_prompt_topics/methods/update)

PUT/accounts/{account_id}/dlp/custom_prompt_topics/{entry_id}

##### [Delete custom prompt topic](/api/resources/zero_trust/subresources/dlp/subresources/custom_prompt_topics/methods/delete)

DELETE/accounts/{account_id}/dlp/custom_prompt_topics/{entry_id}

##### Models

<details>

<summary>

CustomPromptTopic object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

topic: string

maxLength50

minLength2

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

CustomPromptTopicDeleteResponse = unknown

[Link to this property](#)

##### [Fetch all datasets](/api/resources/zero_trust/subresources/dlp/subresources/datasets/methods/list)

GET/accounts/{account_id}/dlp/datasets

##### [Fetch a specific dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/methods/get)

GET/accounts/{account_id}/dlp/datasets/{dataset_id}

##### [Create a new dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/methods/create)

POST/accounts/{account_id}/dlp/datasets

##### [Update details about a dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/methods/update)

PUT/accounts/{account_id}/dlp/datasets/{dataset_id}

##### [Delete a dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/methods/delete)

DELETE/accounts/{account_id}/dlp/datasets/{dataset_id}

##### Models

<details>

<summary>

Dataset object { id, columns, created_at, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

columns: array of object { entry_id, header_name, num_cells, upload_status }

</summary>

entry_id: string

formatuuid

[Link to this property](#)

header_name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

upload_status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

encoding_version: number

formatint32

minimum0

[Link to this property](#)

name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

secret: boolean

[Link to this property](#)

<details>

<summary>

status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

Stores when the dataset was last updated.

This includes name or description changes as well as uploads.

formatdate-time

[Link to this property](#)

<details>

<summary>

uploads: array of object { num_cells, status, version }

</summary>

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

version: number

formatint64

[Link to this property](#)

</details>

[Link to this property](#)

case_sensitive: optional boolean

[Link to this property](#)

description: optional string

The description of the dataset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DatasetArray = array of [Dataset](/api/resources/zero_trust#(resource)%20zero_trust.dlp.datasets%20%3E%20(model)%20dataset%20%3E%20(schema)) { id, columns, created_at, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

columns: array of object { entry_id, header_name, num_cells, upload_status }

</summary>

entry_id: string

formatuuid

[Link to this property](#)

header_name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

upload_status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

encoding_version: number

formatint32

minimum0

[Link to this property](#)

name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

secret: boolean

[Link to this property](#)

<details>

<summary>

status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

Stores when the dataset was last updated.

This includes name or description changes as well as uploads.

formatdate-time

[Link to this property](#)

<details>

<summary>

uploads: array of object { num_cells, status, version }

</summary>

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

version: number

formatint64

[Link to this property](#)

</details>

[Link to this property](#)

case_sensitive: optional boolean

[Link to this property](#)

description: optional string

The description of the dataset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DatasetCreation object { dataset, encoding_version, max_cells, 2 more }

</summary>

dataset: [Dataset](/api/resources/zero_trust#(resource)%20zero_trust.dlp.datasets%20%3E%20(model)%20dataset%20%3E%20(schema)) { id, columns, created_at, 9 more }

[Link to this property](#)

encoding_version: number

Encoding version to use for dataset.

formatint32

minimum0

[Link to this property](#)

max_cells: number

formatint64

minimum0

[Link to this property](#)

version: number

The version to use when uploading the dataset.

formatint64

[Link to this property](#)

secret: optional string

The secret to use for Exact Data Match datasets.

This is not present in Custom Wordlists.

formatpassword

[Link to this property](#)

</details>

[Link to this property](#)

##### [Prepare to upload a new version of a dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/subresources/upload/methods/create)

POST/accounts/{account_id}/dlp/datasets/{dataset_id}/upload

##### [Upload a new version of a dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/subresources/upload/methods/edit)

POST/accounts/{account_id}/dlp/datasets/{dataset_id}/upload/{version}

##### Models

<details>

<summary>

NewVersion object { encoding_version, max_cells, version, 3 more }

</summary>

encoding_version: number

formatint32

minimum0

[Link to this property](#)

max_cells: number

formatint64

minimum0

[Link to this property](#)

version: number

formatint64

[Link to this property](#)

case_sensitive: optional boolean

[Link to this property](#)

<details>

<summary>

columns: optional array of object { entry_id, header_name, num_cells, upload_status }

</summary>

entry_id: string

formatuuid

[Link to this property](#)

header_name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

upload_status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

secret: optional string

formatpassword

[Link to this property](#)

</details>

[Link to this property](#)

##### [Sets the column information for a multi-column upload](/api/resources/zero_trust/subresources/dlp/subresources/datasets/subresources/versions/methods/create)

POST/accounts/{account_id}/dlp/datasets/{dataset_id}/versions/{version}

##### Models

<details>

<summary>

VersionCreateResponse object { entry_id, header_name, num_cells, upload_status }

</summary>

entry_id: string

formatuuid

[Link to this property](#)

header_name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

upload_status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Upload a new version of a multi-column dataset](/api/resources/zero_trust/subresources/dlp/subresources/datasets/subresources/versions/subresources/entries/methods/create)

POST/accounts/{account_id}/dlp/datasets/{dataset_id}/versions/{version}/entries/{entry_id}

##### Models

<details>

<summary>

EntryCreateResponse object { entry_id, header_name, num_cells, upload_status }

</summary>

entry_id: string

formatuuid

[Link to this property](#)

header_name: string

[Link to this property](#)

num_cells: number

formatint64

[Link to this property](#)

<details>

<summary>

upload_status: "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Validate a DLP regex pattern](/api/resources/zero_trust/subresources/dlp/subresources/patterns/methods/validate)

POST/accounts/{account_id}/dlp/patterns/validate

##### Models

<details>

<summary>

PatternValidateResponse object { valid }

</summary>

valid: boolean

[Link to this property](#)

</details>

[Link to this property](#)

##### [Get payload log settings](/api/resources/zero_trust/subresources/dlp/subresources/payload_logs/methods/get)

GET/accounts/{account_id}/dlp/payload_log

##### [Set payload log settings](/api/resources/zero_trust/subresources/dlp/subresources/payload_logs/methods/update)

PUT/accounts/{account_id}/dlp/payload_log

##### Models

<details>

<summary>

PayloadLogGetResponse object { updated_at, masking_level, public_key }

</summary>

updated_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

masking_level: optional "full" or "partial" or "clear" or "default"

Masking level for payload logs.

`full`: The entire payload is masked.

`partial`: Only partial payload content is masked.

`clear`: No masking is applied to the payload content.

`default`: DLP uses its default masking behavior.

</summary>

One of the following:

"full"

[Link to this property](#)

"partial"

[Link to this property](#)

"clear"

[Link to this property](#)

"default"

[Link to this property](#)

</details>

[Link to this property](#)

public_key: optional string

Base64-encoded public key for encrypting payload logs. Null when payload logging is disabled.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PayloadLogUpdateResponse object { updated_at, masking_level, public_key }

</summary>

updated_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

masking_level: optional "full" or "partial" or "clear" or "default"

Masking level for payload logs.

`full`: The entire payload is masked.

`partial`: Only partial payload content is masked.

`clear`: No masking is applied to the payload content.

`default`: DLP uses its default masking behavior.

</summary>

One of the following:

"full"

[Link to this property](#)

"partial"

[Link to this property](#)

"clear"

[Link to this property](#)

"default"

[Link to this property](#)

</details>

[Link to this property](#)

public_key: optional string

Base64-encoded public key for encrypting payload logs. Null when payload logging is disabled.

[Link to this property](#)

</details>

[Link to this property](#)

##### [Get DLP account-level settings.](/api/resources/zero_trust/subresources/dlp/subresources/settings/methods/get)

GET/accounts/{account_id}/dlp/settings

##### [Update DLP account-level settings (full replacement).](/api/resources/zero_trust/subresources/dlp/subresources/settings/methods/update)

PUT/accounts/{account_id}/dlp/settings

##### [Partially update DLP account-level settings.](/api/resources/zero_trust/subresources/dlp/subresources/settings/methods/edit)

PATCH/accounts/{account_id}/dlp/settings

##### [Delete (reset) DLP account-level settings to initial values.](/api/resources/zero_trust/subresources/dlp/subresources/settings/methods/delete)

DELETE/accounts/{account_id}/dlp/settings

##### Models

<details>

<summary>

DLPSettings object { ai_context_analysis, ocr, payload_logging }

DLP account-level settings response.

</summary>

ai_context_analysis: boolean

Whether AI context analysis is enabled at the account level.

[Link to this property](#)

ocr: boolean

Whether OCR is enabled at the account level.

[Link to this property](#)

<details>

<summary>

payload_logging: object { updated_at, masking_level, public_key }

</summary>

updated_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

masking_level: optional "full" or "partial" or "clear" or "default"

Masking level for payload logs.

`full`: The entire payload is masked.

`partial`: Only partial payload content is masked.

`clear`: No masking is applied to the payload content.

`default`: DLP uses its default masking behavior.

</summary>

One of the following:

"full"

[Link to this property](#)

"partial"

[Link to this property](#)

"clear"

[Link to this property](#)

"default"

[Link to this property](#)

</details>

[Link to this property](#)

public_key: optional string

Base64-encoded public key for encrypting payload logs. Null when payload logging is disabled.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Get mapping](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/account_mapping/methods/get)

GET/accounts/{account_id}/dlp/email/account_mapping

##### [Create mapping](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/account_mapping/methods/create)

POST/accounts/{account_id}/dlp/email/account_mapping

##### Models

<details>

<summary>

AccountMappingGetResponse object { addin_identifier_token, auth_requirements }

</summary>

addin_identifier_token: string

formatuuid

[Link to this property](#)

<details>

<summary>

auth_requirements: object { allowed_microsoft_organizations, type } or object { type }

</summary>

One of the following:

<details>

<summary>

object { allowed_microsoft_organizations, type }

</summary>

allowed_microsoft_organizations: array of string

[Link to this property](#)

type: "Org"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

Type object { type }

</summary>

type: "NoAuth"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AccountMappingCreateResponse object { addin_identifier_token, auth_requirements }

</summary>

addin_identifier_token: string

formatuuid

[Link to this property](#)

<details>

<summary>

auth_requirements: object { allowed_microsoft_organizations, type } or object { type }

</summary>

One of the following:

<details>

<summary>

object { allowed_microsoft_organizations, type }

</summary>

allowed_microsoft_organizations: array of string

[Link to this property](#)

type: "Org"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

Type object { type }

</summary>

type: "NoAuth"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [List all email scanner rules](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/list)

GET/accounts/{account_id}/dlp/email/rules

##### [Get an email scanner rule](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/get)

GET/accounts/{account_id}/dlp/email/rules/{rule_id}

##### [Create email scanner rule](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/create)

POST/accounts/{account_id}/dlp/email/rules

##### [Update email scanner rule](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/update)

PUT/accounts/{account_id}/dlp/email/rules/{rule_id}

##### [Delete email scanner rule](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/delete)

DELETE/accounts/{account_id}/dlp/email/rules/{rule_id}

##### [Update email scanner rule priorities](/api/resources/zero_trust/subresources/dlp/subresources/email/subresources/rules/methods/bulk_edit)

PATCH/accounts/{account_id}/dlp/email/rules

##### Models

<details>

<summary>

RuleListResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RuleGetResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RuleCreateResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RuleUpdateResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RuleDeleteResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RuleBulkEditResponse object { action, conditions, created_at, 6 more }

</summary>

<details>

<summary>

action: object { action, message }

</summary>

action: "Block"

[Link to this property](#)

message: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

conditions: array of object { operator, selector, value }

Triggered if all conditions match.

</summary>

<details>

<summary>

operator: "InList" or "NotInList" or "MatchRegex" or "NotMatchRegex"

</summary>

One of the following:

"InList"

[Link to this property](#)

"NotInList"

[Link to this property](#)

"MatchRegex"

[Link to this property](#)

"NotMatchRegex"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

selector: "Recipients" or "Sender" or "DLPProfiles"

</summary>

One of the following:

"Recipients"

[Link to this property](#)

"Sender"

[Link to this property](#)

"DLPProfiles"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

value: array of string or string

</summary>

One of the following:

array of string

[Link to this property](#)

string

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

priority: number

formatint32

minimum0

[Link to this property](#)

rule_id: string

formatuuid

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

##### [List all profiles](/api/resources/zero_trust/subresources/dlp/subresources/profiles/methods/list)

GET/accounts/{account_id}/dlp/profiles

##### [Get DLP Profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/methods/get)

GET/accounts/{account_id}/dlp/profiles/{profile_id}

##### Models

<details>

<summary>

ContextAwareness object { enabled, skip }

Scan the context of predefined entries to only return matches surrounded by keywords.

</summary>

enabled: boolean

If true, scan the context of predefined entries to only return matches surrounded by keywords.

[Link to this property](#)

skip: [SkipConfiguration](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles%20%3E%20(model)%20skip_configuration%20%3E%20(schema)) { files }

Content types to exclude from context analysis and return all matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

Profile = object { id, allowed_match_count, created_at, 13 more } or object { id, allowed_match_count, entries, 7 more } or object { id, created_at, entries, 6 more }

</summary>

One of the following:

<details>

<summary>

CustomProfile object { id, allowed_match_count, created_at, 13 more }

</summary>

id: string

The id of the profile (uuid).

formatuuid

[Link to this property](#)

allowed_match_count: number

Related DLP policies will trigger when the match count exceeds the number set.

formatint32

maximum1000

minimum0

[Link to this property](#)

created_at: string

When the profile was created.

formatdate-time

[Link to this property](#)

name: string

The name of the profile.

[Link to this property](#)

ocr_enabled: boolean

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

When the profile was lasted updated.

formatdate-time

[Link to this property](#)

ai_context_enabled: optional boolean

[Link to this property](#)

<details>

<summary>

confidence_threshold: optional "low" or "medium" or "high" or "very_high"

</summary>

One of the following:

"low"

[Link to this property](#)

"medium"

[Link to this property](#)

"high"

[Link to this property](#)

"very_high"

[Link to this property](#)

</details>

[Link to this property](#)

Deprecatedcontext_awareness: optional [ContextAwareness](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles%20%3E%20(model)%20context_awareness%20%3E%20(schema)) { enabled, skip }

Scan the context of predefined entries to only return matches surrounded by keywords.

[Link to this property](#)

data_classes: optional array of string

Data classes associated with this profile.

[Link to this property](#)

data_tags: optional array of string

Data tags associated with this profile.

[Link to this property](#)

description: optional string

The description of the profile.

[Link to this property](#)

<details>

<summary>

Deprecatedentries: optional array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

sensitivity_levels: optional array of object { group_id, level_id }

Sensitivity levels associated with this profile.

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

shared_entries: optional array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedProfile object { id, allowed_match_count, entries, 7 more }

</summary>

id: string

The id of the predefined profile (uuid).

formatuuid

[Link to this property](#)

allowed_match_count: number

formatint32

[Link to this property](#)

<details>

<summary>

Deprecatedentries: array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

name: string

The name of the predefined profile.

[Link to this property](#)

type: "predefined"

[Link to this property](#)

ai_context_enabled: optional boolean

[Link to this property](#)

<details>

<summary>

confidence_threshold: optional "low" or "medium" or "high" or "very_high"

</summary>

One of the following:

"low"

[Link to this property](#)

"medium"

[Link to this property](#)

"high"

[Link to this property](#)

"very_high"

[Link to this property](#)

</details>

[Link to this property](#)

Deprecatedcontext_awareness: optional [ContextAwareness](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles%20%3E%20(model)%20context_awareness%20%3E%20(schema)) { enabled, skip }

Scan the context of predefined entries to only return matches surrounded by keywords.

[Link to this property](#)

ocr_enabled: optional boolean

[Link to this property](#)

open_access: optional boolean

Whether this profile can be accessed by anyone.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationProfile object { id, created_at, entries, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

Deprecatedentries: array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

integration_id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

shared_entries: array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The description of the profile.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipConfiguration object { files }

Content types to exclude from context analysis and return all matches.

</summary>

files: boolean

If the content type is a file, skip context analysis and return all matches.

[Link to this property](#)

</details>

[Link to this property](#)

##### [Get custom profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/custom/methods/get)

GET/accounts/{account_id}/dlp/profiles/custom/{profile_id}

##### [Create custom profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/custom/methods/create)

POST/accounts/{account_id}/dlp/profiles/custom

##### [Update custom profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/custom/methods/update)

PUT/accounts/{account_id}/dlp/profiles/custom/{profile_id}

##### [Delete custom profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/custom/methods/delete)

DELETE/accounts/{account_id}/dlp/profiles/custom/{profile_id}

##### Models

<details>

<summary>

CustomProfile object { id, allowed_match_count, created_at, 12 more }

</summary>

id: string

The id of the profile (uuid).

formatuuid

[Link to this property](#)

allowed_match_count: number

Related DLP policies will trigger when the match count exceeds the number set.

formatint32

maximum1000

minimum0

[Link to this property](#)

created_at: string

When the profile was created.

formatdate-time

[Link to this property](#)

name: string

The name of the profile.

[Link to this property](#)

ocr_enabled: boolean

[Link to this property](#)

updated_at: string

When the profile was lasted updated.

formatdate-time

[Link to this property](#)

ai_context_enabled: optional boolean

[Link to this property](#)

<details>

<summary>

confidence_threshold: optional "low" or "medium" or "high" or "very_high"

</summary>

One of the following:

"low"

[Link to this property](#)

"medium"

[Link to this property](#)

"high"

[Link to this property](#)

"very_high"

[Link to this property](#)

</details>

[Link to this property](#)

Deprecatedcontext_awareness: optional [ContextAwareness](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles%20%3E%20(model)%20context_awareness%20%3E%20(schema)) { enabled, skip }

Scan the context of predefined entries to only return matches surrounded by keywords.

[Link to this property](#)

data_classes: optional array of string

Data classes associated with this profile.

[Link to this property](#)

data_tags: optional array of string

Data tags associated with this profile.

[Link to this property](#)

description: optional string

The description of the profile.

[Link to this property](#)

<details>

<summary>

Deprecatedentries: optional array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

sensitivity_levels: optional array of object { group_id, level_id }

Sensitivity levels associated with this profile.

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

shared_entries: optional array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

Pattern object { regex, validation }

</summary>

regex: string

[Link to this property](#)

Deprecatedvalidation: optional "luhn"

[Link to this property](#)

</details>

[Link to this property](#)

CustomDeleteResponse = unknown

[Link to this property](#)

##### [Get predefined profile config](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/predefined/methods/get)

GET/accounts/{account_id}/dlp/profiles/predefined/{profile_id}/config

##### [Update predefined profile config](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/predefined/methods/update)

PUT/accounts/{account_id}/dlp/profiles/predefined/{profile_id}/config

##### [Delete predefined profile](/api/resources/zero_trust/subresources/dlp/subresources/profiles/subresources/predefined/methods/delete)

DELETE/accounts/{account_id}/dlp/profiles/predefined/{profile_id}

##### Models

<details>

<summary>

PredefinedProfile object { id, allowed_match_count, confidence_threshold, 6 more }

</summary>

id: string

The id of the predefined profile (uuid).

formatuuid

[Link to this property](#)

allowed_match_count: number

formatint32

[Link to this property](#)

confidence_threshold: string

[Link to this property](#)

enabled_entries: array of string

Entries to enable for this predefined profile. Any entries not provided will be disabled.

[Link to this property](#)

<details>

<summary>

Deprecatedentries: array of object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

This field has been deprecated for `enabled_entries`.

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

name: string

The name of the predefined profile.

[Link to this property](#)

ai_context_enabled: optional boolean

[Link to this property](#)

ocr_enabled: optional boolean

[Link to this property](#)

open_access: optional boolean

Whether this profile can be accessed by anyone.

[Link to this property](#)

</details>

[Link to this property](#)

PredefinedDeleteResponse = unknown

[Link to this property](#)

##### [Fetch limits associated with DLP for account](/api/resources/zero_trust/subresources/dlp/subresources/limits/methods/list)

GET/accounts/{account_id}/dlp/limits

##### Models

<details>

<summary>

LimitListResponse object { max_custom_regex_entries, max_dataset_cells, max_document_fingerprints, 3 more }

</summary>

max_custom_regex_entries: number

Maximum number of custom regex entries allowed for the account.

formatint64

minimum0

[Link to this property](#)

max_dataset_cells: number

Maximum number of dataset cells allowed for the account, across all EDM and CWL datasets.

formatint64

minimum0

[Link to this property](#)

max_document_fingerprints: number

Maximum number of document fingerprints allowed for the account.

formatint64

minimum0

[Link to this property](#)

used_custom_regex_entries: number

Number of custom regex entries currently configured for the account.

formatint64

minimum0

[Link to this property](#)

used_dataset_cells: number

Number of dataset cells currently configured for the account, across all EDM and CWL datasets. Document fingerprints do not count towards this limit.

formatint64

minimum0

[Link to this property](#)

used_document_fingerprints: number

Number of document fingerprints currently configured for the account.

formatint64

minimum0

[Link to this property](#)

</details>

[Link to this property](#)

##### [List all entries](/api/resources/zero_trust/subresources/dlp/subresources/entries/methods/list)

GET/accounts/{account_id}/dlp/entries

##### [Get DLP Entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/methods/get)

GET/accounts/{account_id}/dlp/entries/{entry_id}

##### [Create custom entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/methods/create)

POST/accounts/{account_id}/dlp/entries

##### [Update entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/methods/update)

PUT/accounts/{account_id}/dlp/entries/{entry_id}

##### [Delete custom entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/methods/delete)

DELETE/accounts/{account_id}/dlp/entries/{entry_id}

##### Models

<details>

<summary>

EntryListResponse = object { id, created_at, enabled, 8 more } or object { id, created_at, enabled, 5 more } or object { id, confidence, enabled, 6 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

EntryGetResponse = object { id, created_at, enabled, 9 more } or object { id, created_at, enabled, 6 more } or object { id, confidence, enabled, 7 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

EntryCreateResponse object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

EntryUpdateResponse = object { id, created_at, enabled, 7 more } or object { id, created_at, enabled, 4 more } or object { id, confidence, enabled, 5 more } or 4 more

</summary>

One of the following:

<details>

<summary>

CustomEntry object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomPromptTopicEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedEntry object { id, confidence, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExactDataEntry object { id, case_sensitive, created_at, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DocumentFingerprintEntry object { id, created_at, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

WordListEntry object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

EntryDeleteResponse = unknown

[Link to this property](#)

##### [Create custom entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/custom/methods/create)

POST/accounts/{account_id}/dlp/entries

##### [Update custom entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/custom/methods/update)

PUT/accounts/{account_id}/dlp/entries/custom/{entry_id}

##### [Delete custom entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/custom/methods/delete)

DELETE/accounts/{account_id}/dlp/entries/{entry_id}

##### [Get DLP Entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/custom/methods/get)

GET/accounts/{account_id}/dlp/entries/{entry_id}

##### [List all entries](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/custom/methods/list)

GET/accounts/{account_id}/dlp/entries

##### Models

<details>

<summary>

CustomCreateResponse object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomUpdateResponse object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

CustomDeleteResponse = unknown

[Link to this property](#)

<details>

<summary>

CustomGetResponse = object { id, created_at, enabled, 9 more } or object { id, created_at, enabled, 6 more } or object { id, confidence, enabled, 7 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

CustomListResponse = object { id, created_at, enabled, 8 more } or object { id, created_at, enabled, 5 more } or object { id, confidence, enabled, 6 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Create predefined entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/predefined/methods/create)

POST/accounts/{account_id}/dlp/entries/predefined

##### [Update predefined entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/predefined/methods/update)

PUT/accounts/{account_id}/dlp/entries/predefined/{entry_id}

##### [Delete predefined entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/predefined/methods/delete)

DELETE/accounts/{account_id}/dlp/entries/predefined/{entry_id}

##### [Get DLP Entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/predefined/methods/get)

GET/accounts/{account_id}/dlp/entries/{entry_id}

##### [List all entries](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/predefined/methods/list)

GET/accounts/{account_id}/dlp/entries

##### Models

<details>

<summary>

PredefinedCreateResponse object { id, confidence, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedUpdateResponse object { id, confidence, enabled, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

PredefinedDeleteResponse = unknown

[Link to this property](#)

<details>

<summary>

PredefinedGetResponse = object { id, created_at, enabled, 9 more } or object { id, created_at, enabled, 6 more } or object { id, confidence, enabled, 7 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

PredefinedListResponse = object { id, created_at, enabled, 8 more } or object { id, created_at, enabled, 5 more } or object { id, confidence, enabled, 6 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Create integration entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/integration/methods/create)

POST/accounts/{account_id}/dlp/entries/integration

##### [Update integration entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/integration/methods/update)

PUT/accounts/{account_id}/dlp/entries/integration/{entry_id}

##### [Delete integration entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/integration/methods/delete)

DELETE/accounts/{account_id}/dlp/entries/integration/{entry_id}

##### [Get DLP Entry](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/integration/methods/get)

GET/accounts/{account_id}/dlp/entries/{entry_id}

##### [List all entries](/api/resources/zero_trust/subresources/dlp/subresources/entries/subresources/integration/methods/list)

GET/accounts/{account_id}/dlp/entries

##### Models

<details>

<summary>

IntegrationCreateResponse object { id, created_at, enabled, 3 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationUpdateResponse object { id, created_at, enabled, 3 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

IntegrationDeleteResponse = unknown

[Link to this property](#)

<details>

<summary>

IntegrationGetResponse = object { id, created_at, enabled, 9 more } or object { id, created_at, enabled, 6 more } or object { id, confidence, enabled, 7 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 9 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

profiles: optional array of object { id, name }

</summary>

id: string

formatuuid

[Link to this property](#)

name: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

IntegrationListResponse = object { id, created_at, enabled, 8 more } or object { id, created_at, enabled, 5 more } or object { id, confidence, enabled, 6 more } or 4 more

</summary>

One of the following:

<details>

<summary>

object { id, created_at, enabled, 8 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

pattern: [Pattern](/api/resources/zero_trust#(resource)%20zero_trust.dlp.profiles.custom%20%3E%20(model)%20pattern%20%3E%20(schema)) { regex, validation }

[Link to this property](#)

type: "custom"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

validator_ids: optional array of string

Validators this entry references, by id, at most 10. An empty list means the entry references none.

Returned by the entry endpoints. Not returned on entries embedded in other responses, such as profiles.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

Deprecatedenabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "custom_prompt_topic"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the custom prompt topic entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, confidence, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

<details>

<summary>

confidence: object { ai_context_available, available }

</summary>

ai_context_available: boolean

Indicates whether this entry has AI remote service validation.

[Link to this property](#)

available: boolean

Indicates whether this entry has any form of validation that is not an AI remote service.

[Link to this property](#)

</details>

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "predefined"

[Link to this property](#)

deprecated: optional boolean

Whether this entry is deprecated for new use. This is computed from the static catalog and emitted only when true.

[Link to this property](#)

Deprecatedprofile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

variant: optional object { topic_type, type, description } or object { type, description }

A Predefined AI prompt classification topic entry.

</summary>

One of the following:

<details>

<summary>

object { topic_type, type, description }

A Predefined AI prompt classification topic entry.

</summary>

<details>

<summary>

topic_type: "Intent" or "Content"

</summary>

One of the following:

"Intent"

[Link to this property](#)

"Content"

[Link to this property](#)

</details>

[Link to this property](#)

type: "PromptTopic"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined AI prompt topic represents.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { type, description }

A general predefined entry.

</summary>

type: "General"

[Link to this property](#)

description: optional string

A customer-facing explanation of what this predefined entry represents.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "integration"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, case_sensitive, created_at, 7 more }

</summary>

id: string

formatuuid

[Link to this property](#)

case_sensitive: boolean

Only applies to custom word lists. Determines if the words should be matched in a case-sensitive manner Cannot be set to false if secret is true

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

secret: boolean

[Link to this property](#)

type: "exact_data"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the exact data entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "document_fingerprint"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

The optional description of the document fingerprint entry.

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, created_at, enabled, 6 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

enabled: boolean

[Link to this property](#)

name: string

[Link to this property](#)

type: "word_list"

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

word_list: array of string

[Link to this property](#)

profile_id: optional string

formatuuid

[Link to this property](#)

<details>

<summary>

upload_status: optional "empty" or "uploading" or "pending" or 3 more

</summary>

One of the following:

"empty"

[Link to this property](#)

"uploading"

[Link to this property](#)

"pending"

[Link to this property](#)

"processing"

[Link to this property](#)

"failed"

[Link to this property](#)

"complete"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

##### [Retrieve all sensitivity groups in an account](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/methods/list)

GET/accounts/{account_id}/dlp/sensitivity_groups

##### [Retrieve a specific sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/methods/get)

GET/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}

##### [Creates a new sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/methods/create)

POST/accounts/{account_id}/dlp/sensitivity_groups

##### [Update the attributes of a single sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/methods/update)

PUT/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}

##### [Delete a single sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/methods/delete)

DELETE/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}

##### Models

<details>

<summary>

SensitivityGroupListResponse object { id, created_at, levels, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

levels: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SensitivityGroupGetResponse object { id, created_at, levels, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

levels: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SensitivityGroupCreateResponse object { id, created_at, levels, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

levels: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SensitivityGroupUpdateResponse object { id, created_at, levels, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

<details>

<summary>

levels: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

SensitivityGroupDeleteResponse = unknown

[Link to this property](#)

##### [Retrieve all sensitivity levels in a sensitivity group](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/methods/list)

GET/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/levels

##### [Retrieve a specific sensitivity level.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/methods/get)

GET/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/levels/{sensitivity_level_id}

##### [Creates a new sensitivity level.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/methods/create)

POST/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/levels

##### [Update the attributes of a single sensitivity level.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/methods/update)

PUT/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/levels/{sensitivity_level_id}

##### [Delete a single sensitivity level.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/methods/delete)

DELETE/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/levels/{sensitivity_level_id}

##### Models

<details>

<summary>

LevelListResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LevelGetResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LevelCreateResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LevelUpdateResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

LevelDeleteResponse = unknown

[Link to this property](#)

##### [Retrieve the ordered list of level IDs for a sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/subresources/order/methods/get)

GET/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/level_order

##### [Set the ordering of levels within a sensitivity group.](/api/resources/zero_trust/subresources/dlp/subresources/sensitivity_groups/subresources/levels/subresources/order/methods/update)

PUT/accounts/{account_id}/dlp/sensitivity_groups/{sensitivity_group_id}/level_order

##### Models

<details>

<summary>

OrderGetResponse object { level_ids }

The ordered list of level IDs for a sensitivity group. Used to get and set the ordering of levels independently of level attributes.

</summary>

level_ids: array of string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

OrderUpdateResponse object { level_ids }

The ordered list of level IDs for a sensitivity group. Used to get and set the ordering of levels independently of level attributes.

</summary>

level_ids: array of string

[Link to this property](#)

</details>

[Link to this property](#)

##### [Retrieve all data tag categories in an account](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/methods/list)

GET/accounts/{account_id}/dlp/data_tag_categories

##### [Retrieve a specific data tag category.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/methods/get)

GET/accounts/{account_id}/dlp/data_tag_categories/{category_id}

##### [Creates a new data tag category.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/methods/create)

POST/accounts/{account_id}/dlp/data_tag_categories

##### [Update the attributes of a single data tag category.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/methods/update)

PUT/accounts/{account_id}/dlp/data_tag_categories/{category_id}

##### [Delete a single data tag category.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/methods/delete)

DELETE/accounts/{account_id}/dlp/data_tag_categories/{category_id}

##### Models

<details>

<summary>

DataTagCategoryListResponse object { id, created_at, name, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

tags: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagCategoryGetResponse object { id, created_at, name, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

tags: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagCategoryCreateResponse object { id, created_at, name, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

tags: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagCategoryUpdateResponse object { id, created_at, name, 4 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

tags: array of object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

template_id: optional string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

DataTagCategoryDeleteResponse = unknown

[Link to this property](#)

##### [Retrieve all data tags in a data tag category](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/subresources/data_tags/methods/list)

GET/accounts/{account_id}/dlp/data_tag_categories/{category_id}/data_tags

##### [Retrieve a specific data tag.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/subresources/data_tags/methods/get)

GET/accounts/{account_id}/dlp/data_tag_categories/{category_id}/data_tags/{tag_id}

##### [Creates a new data tag.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/subresources/data_tags/methods/create)

POST/accounts/{account_id}/dlp/data_tag_categories/{category_id}/data_tags

##### [Update the attributes of a single data tag.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/subresources/data_tags/methods/update)

PUT/accounts/{account_id}/dlp/data_tag_categories/{category_id}/data_tags/{tag_id}

##### [Delete a single data tag.](/api/resources/zero_trust/subresources/dlp/subresources/data_tag_categories/subresources/data_tags/methods/delete)

DELETE/accounts/{account_id}/dlp/data_tag_categories/{category_id}/data_tags/{tag_id}

##### Models

<details>

<summary>

DataTagListResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagGetResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagCreateResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataTagUpdateResponse object { id, created_at, name, 2 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

name: string

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

DataTagDeleteResponse = unknown

[Link to this property](#)

##### [Retrieve all data classes in an account](/api/resources/zero_trust/subresources/dlp/subresources/data_classes/methods/list)

GET/accounts/{account_id}/dlp/data_classes

##### [Retrieve a specific data class](/api/resources/zero_trust/subresources/dlp/subresources/data_classes/methods/get)

GET/accounts/{account_id}/dlp/data_classes/{data_class_id}

##### [Creates a new data class](/api/resources/zero_trust/subresources/dlp/subresources/data_classes/methods/create)

POST/accounts/{account_id}/dlp/data_classes

##### [Update the attributes of a single data class](/api/resources/zero_trust/subresources/dlp/subresources/data_classes/methods/update)

PUT/accounts/{account_id}/dlp/data_classes/{data_class_id}

##### [Delete a single data class](/api/resources/zero_trust/subresources/dlp/subresources/data_classes/methods/delete)

DELETE/accounts/{account_id}/dlp/data_classes/{data_class_id}

##### Models

<details>

<summary>

DataClassListResponse object { id, created_at, data_tags, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

data_tags: array of string

[Link to this property](#)

expression: string

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

sensitivity_levels: array of object { group_id, level_id }

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataClassGetResponse object { id, created_at, data_tags, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

data_tags: array of string

[Link to this property](#)

expression: string

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

sensitivity_levels: array of object { group_id, level_id }

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataClassCreateResponse object { id, created_at, data_tags, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

data_tags: array of string

[Link to this property](#)

expression: string

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

sensitivity_levels: array of object { group_id, level_id }

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DataClassUpdateResponse object { id, created_at, data_tags, 5 more }

</summary>

id: string

formatuuid

[Link to this property](#)

created_at: string

formatdate-time

[Link to this property](#)

data_tags: array of string

[Link to this property](#)

expression: string

[Link to this property](#)

name: string

[Link to this property](#)

<details>

<summary>

sensitivity_levels: array of object { group_id, level_id }

</summary>

group_id: string

formatuuid

[Link to this property](#)

level_id: string

formatuuid

[Link to this property](#)

</details>

[Link to this property](#)

updated_at: string

formatdate-time

[Link to this property](#)

description: optional string

[Link to this property](#)

</details>

[Link to this property](#)

DataClassDeleteResponse = unknown

[Link to this property](#)
