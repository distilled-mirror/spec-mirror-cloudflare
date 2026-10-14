---
title: Secrets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Basic Auth Credentials](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Secrets

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