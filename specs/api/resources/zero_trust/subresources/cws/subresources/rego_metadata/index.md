---
title: Rego Metadata
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Rego Metadata

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