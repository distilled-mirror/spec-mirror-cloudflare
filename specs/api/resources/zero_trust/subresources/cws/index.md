---
title: Cloud Workload Security
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Cloud Workload Security

#### Cloud Workload SecurityBasic Auth Credentials

##### [List basic-auth credentials for an account](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/methods/list)

GET/accounts/{account\_id}/cws/basic-auth-credentials

##### [Get a basic-auth credential by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/methods/get)

GET/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}

##### [Create a basic-auth credential](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/methods/create)

POST/accounts/{account\_id}/cws/basic-auth-credentials

##### [Delete a basic-auth credential](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/methods/delete)

DELETE/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}

##### ModelsExpand Collapse

<details>

<summary>

BasicAuthCredential object {id, created\_at, updated\_at, username }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

username: string

Login presented by the client. Printable ASCII only, excluding space and colon (RFC 7617 forbids a colon in the user-id).

maxLength100

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials%20%3E%20(model)%20basic_auth_credential%20%3E%20(schema)>)

<details>

<summary>

BasicAuthCredentialDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials%20%3E%20(model)%20basic_auth_credential_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityBasic Auth CredentialsSecrets

##### [List secrets for a basic-auth credential](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/subresources/secrets/methods/list)

GET/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}/secrets

##### [Get a basic-auth secret by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/subresources/secrets/methods/get)

GET/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}/secrets/{secret\_id}

##### [Add a secret to a basic-auth credential](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/subresources/secrets/methods/create)

POST/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}/secrets

##### [Delete a basic-auth secret](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/subresources/secrets/methods/delete)

DELETE/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}/secrets/{secret\_id}

##### ModelsExpand Collapse

<details>

<summary>

BasicAuthSecret object {id, created\_at, expires\_at }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

expires\_at: optional string

Optional RFC 3339 expiration time. Omit for no expiration.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(model)%20basic_auth_secret%20%3E%20(schema)>)

<details>

<summary>

SecretDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(model)%20secret_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityDeployments

##### [List deployments](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/list)

GET/accounts/{account\_id}/cws/deployments

##### [Get a deployment by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/get)

GET/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### [Create a new deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/create)

POST/accounts/{account\_id}/cws/deployments

##### [Update a deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/update)

PUT/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### [Delete a deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/delete)

DELETE/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### ModelsExpand Collapse

<details>

<summary>

Deployment object {id, basic\_auth\_credential\_ids, created\_at, 9 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

basic\_auth\_credential\_ids: array of string

IDs of basic-auth credentials attached to this deployment

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

default\_mode: "ALLOW"or "BLOCK"

Default traffic decision when no policy set matches

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

on\_error\_action: "BLOCK"or "SKIP"

Action applied when an enforcing policy has a runtime Rego error

</summary>

One of the following:

"BLOCK"

<a href="#">Link to this property</a>

"SKIP"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

policy\_set\_ids: array of string

IDs of policy sets attached to this deployment

<a href="#">Link to this property</a>

rego\_raise\_error: boolean

Whether OPA builtin failures are raised as runtime evaluation errors

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this deployment

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

domain\_acl\_id: optional string

ID of the attached domain ACL. Omitted when none.

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(model)%20deployment%20%3E%20(schema)>)

<details>

<summary>

DeploymentDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(model)%20deployment_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityDomain ACLs

##### [List domain ACLs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/list)

GET/accounts/{account\_id}/cws/domain-acls

##### [Get a domain ACL by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/get)

GET/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### [Create a new domain ACL](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/create)

POST/accounts/{account\_id}/cws/domain-acls

##### [Update a domain ACL and replace its entries](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/update)

PUT/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### [Delete a domain ACL](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/delete)

DELETE/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### ModelsExpand Collapse

<details>

<summary>

DomainACL object {id, created\_at, default\_action, 3 more }

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

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(model)%20domain_acl%20%3E%20(schema)>)

<details>

<summary>

DomainACLDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(model)%20domain_acl_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityPolicies

##### [List policies](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/list)

GET/accounts/{account\_id}/cws/policies

##### [Get a policy by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/get)

GET/accounts/{account\_id}/cws/policies/{policy\_id}

##### [Create a new policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/create)

POST/accounts/{account\_id}/cws/policies

##### [Update a policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/update)

PUT/accounts/{account\_id}/cws/policies/{policy\_id}

##### [Delete a policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/delete)

DELETE/accounts/{account\_id}/cws/policies/{policy\_id}

##### ModelsExpand Collapse

<details>

<summary>

Policy object {id, created\_at, entrypoint, 7 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

entrypoint: string

Non-function rule declared in rego\_source. Evaluation uses data.&lt;package\_path&gt;..

maxLength255

<a href="#">Link to this property</a>

filter: string

Filter expression that determines whether this policy applies. Maximum 4096 UTF-8 bytes.

maxLength4096

minLength1

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

package\_path: string

Dotted path derived from rego\_source. Begins with policy. and is unique per account.

maxLength1024

<a href="#">Link to this property</a>

rego\_source: string

Inline Rego source with a package beginning with “policy.” Maximum 16384 UTF-8 bytes.

maxLength16384

minLength1

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this policy

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(model)%20policy%20%3E%20(schema)>)

<details>

<summary>

PolicyDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(model)%20policy_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityPolicy Sets

##### [List policy sets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/list)

GET/accounts/{account\_id}/cws/policy-sets

##### [Get a policy set by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/get)

GET/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### [Create a new policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/create)

POST/accounts/{account\_id}/cws/policy-sets

##### [Update a policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/update)

PUT/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### [Delete a policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/delete)

DELETE/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### ModelsExpand Collapse

<details>

<summary>

PolicySet object {id, created\_at, exclude\_workload\_ids, 6 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

exclude\_workload\_ids: array of string

IDs of workloads that exclude matching requests. Exclusions take precedence.

<a href="#">Link to this property</a>

include\_workload\_ids: array of string

IDs of workloads that include matching requests. Empty includes all requests before exclusions.

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

policies: array of object {enforce, policy\_id }

Member policies and their per-membership enforcement mode

</summary>

enforce: boolean

Whether this policy should enforce when it matches. False keeps the policy attached for non-enforcing evaluation.

<a href="#">Link to this property</a>

policy\_id: string

ID of the member policy

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this policy set

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(model)%20policy_set%20%3E%20(schema)>)

<details>

<summary>

PolicySetDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(model)%20policy_set_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityRego Metadata

##### [List Rego metadata documents](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_metadata/methods/list)

GET/accounts/{account\_id}/cws/rego-metadata

##### [Get a rego metadata document by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_metadata/methods/get)

GET/accounts/{account\_id}/cws/rego-metadata/{rego\_metadata\_id}

##### [Create a new rego metadata document](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_metadata/methods/create)

POST/accounts/{account\_id}/cws/rego-metadata

##### [Update a rego metadata document](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_metadata/methods/update)

PUT/accounts/{account\_id}/cws/rego-metadata/{rego\_metadata\_id}

##### [Delete a rego metadata document](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_metadata/methods/delete)

DELETE/accounts/{account\_id}/cws/rego-metadata/{rego\_metadata\_id}

##### ModelsExpand Collapse

<details>

<summary>

RegoMetadata object {id, created\_at, data, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

data: unknown

<a href="#">Link to this property</a>

import\_path: string

Unique Rego import path in the form metadata., with one alphanumeric or underscore segment. Reference it as data.&lt;import\_path&gt;.

maxLength255

minLength1

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

[Link to this property](#)%20zero_trust.cws.rego_metadata%20%3E%20(model)%20rego_metadata%20%3E%20(schema)>)

<details>

<summary>

RegoMetadataDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.rego_metadata%20%3E%20(model)%20rego_metadata_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityRego Modules

##### [List Rego modules](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/list)

GET/accounts/{account\_id}/cws/rego-modules

##### [Get a Rego module by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/get)

GET/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### [Create a new Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/create)

POST/accounts/{account\_id}/cws/rego-modules

##### [Update a Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/update)

PUT/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### [Delete a Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/delete)

DELETE/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### ModelsExpand Collapse

<details>

<summary>

RegoModule object {id, created\_at, name, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

package\_path: string

Dotted path derived from rego\_source. Begins with lib. and is unique per account.

maxLength1024

<a href="#">Link to this property</a>

rego\_source: string

Library Rego source with a package beginning with “lib.” Maximum 16384 UTF-8 bytes.

maxLength16384

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.rego_modules%20%3E%20(model)%20rego_module%20%3E%20(schema)>)

<details>

<summary>

RegoModuleDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.rego_modules%20%3E%20(model)%20rego_module_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityTenant Structures

##### [List tenant structures for an account](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/list)

GET/accounts/{account\_id}/cws/tenant-structures

##### [Get a tenant structure by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/get)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### [Create a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/create)

POST/accounts/{account\_id}/cws/tenant-structures

##### [Update a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/update)

PUT/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### [Delete a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/delete)

DELETE/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### ModelsExpand Collapse

<details>

<summary>

TenantStructure object {id, application, created\_at, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

application: "aws"or "cloudflare"

Platform this structure models. Immutable after creation; determines valid node kinds and identifier formats.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"cloudflare"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

import\_path: optional string

Optional unique Rego mount path in the form tenant... The application segment must match application; omitted when unmounted.

maxLength255

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures%20%3E%20(model)%20tenant_structure%20%3E%20(schema)>)

<details>

<summary>

TenantStructureDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures%20%3E%20(model)%20tenant_structure_delete_response%20%3E%20(schema)>)

#### Cloud Workload SecurityTenant StructuresNodes

##### [List nodes for a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/list)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes

##### [Get a tenant node by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/get)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Add a node to a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/create)

POST/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes

##### [Update a tenant node](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/update)

PUT/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Delete a tenant node](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/delete)

DELETE/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Apply a batch of tenant node mutations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/batch)

POST/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/batch

##### ModelsExpand Collapse

<details>

<summary>

TenantStructureNode object {id, created\_at, native\_id, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

native\_id: string

Cloud-native identifier of this node, unique within the structure; the parent-reference target. Shape depends on the structure’s application. Immutable after create.

maxLength255

minLength1

<a href="#">Link to this property</a>

node\_kind: string

Position in the tree. Legal values depend on the structure’s application (aws: root/ou/account; cloudflare: org/account/zone). At most one root per structure. Immutable after create.

maxLength64

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Display name (e.g. an OU or account name), mutable. Optional; empty by default.

maxLength100

<a href="#">Link to this property</a>

parent: optional string

Native ID of this node’s parent. Required for non-root nodes and omitted for the root. The parent must be in the same structure and able to contain this node kind.

maxLength255

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)>)

<details>

<summary>

NodeDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20node_delete_response%20%3E%20(schema)>)

<details>

<summary>

NodeBatchResponse object {created, deleted, updated }

</summary>

<details>

<summary>

created: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)">TenantStructureNode</a> { id, created\_at, native\_id, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

native\_id: string

Cloud-native identifier of this node, unique within the structure; the parent-reference target. Shape depends on the structure’s application. Immutable after create.

maxLength255

minLength1

<a href="#">Link to this property</a>

node\_kind: string

Position in the tree. Legal values depend on the structure’s application (aws: root/ou/account; cloudflare: org/account/zone). At most one root per structure. Immutable after create.

maxLength64

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Display name (e.g. an OU or account name), mutable. Optional; empty by default.

maxLength100

<a href="#">Link to this property</a>

parent: optional string

Native ID of this node’s parent. Required for non-root nodes and omitted for the root. The parent must be in the same structure and able to contain this node kind.

maxLength255

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

deleted: array of object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)">TenantStructureNode</a> { id, created\_at, native\_id, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

native\_id: string

Cloud-native identifier of this node, unique within the structure; the parent-reference target. Shape depends on the structure’s application. Immutable after create.

maxLength255

minLength1

<a href="#">Link to this property</a>

node\_kind: string

Position in the tree. Legal values depend on the structure’s application (aws: root/ou/account; cloudflare: org/account/zone). At most one root per structure. Immutable after create.

maxLength64

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Display name (e.g. an OU or account name), mutable. Optional; empty by default.

maxLength100

<a href="#">Link to this property</a>

parent: optional string

Native ID of this node’s parent. Required for non-root nodes and omitted for the root. The parent must be in the same structure and able to contain this node kind.

maxLength255

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20node_batch_response%20%3E%20(schema)>)

#### Cloud Workload SecurityWorkloads

##### [List workloads](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/list)

GET/accounts/{account\_id}/cws/workloads

##### [Get a workload by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/get)

GET/accounts/{account\_id}/cws/workloads/{workload\_id}

##### [Create a new workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/create)

POST/accounts/{account\_id}/cws/workloads

##### [Update a workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/update)

PUT/accounts/{account\_id}/cws/workloads/{workload\_id}

##### [Delete a workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/delete)

DELETE/accounts/{account\_id}/cws/workloads/{workload\_id}

##### ModelsExpand Collapse

<details>

<summary>

Workload object {id, created\_at, filter, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

filter: string

Filter expression selecting the requests this workload matches. Maximum 4096 UTF-8 bytes.

maxLength4096

minLength1

<a href="#">Link to this property</a>

name: string

Human-readable handle; unique per account.

maxLength100

minLength1

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this workload

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.workloads%20%3E%20(model)%20workload%20%3E%20(schema)>)

<details>

<summary>

WorkloadDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.workloads%20%3E%20(model)%20workload_delete_response%20%3E%20(schema)>)