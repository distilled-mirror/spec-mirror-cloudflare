---
title: Registries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Registries

##### [Get the list of configured registries in the account](https://developers.cloudflare.com/api/resources/containers/subresources/registries/methods/list)

GET/accounts/{account\_id}/containers/registries

##### [Configure a private external image registry](https://developers.cloudflare.com/api/resources/containers/subresources/registries/methods/create)

POST/accounts/{account\_id}/containers/registries

##### [Delete a registry from the account](https://developers.cloudflare.com/api/resources/containers/subresources/registries/methods/delete)

DELETE/accounts/{account\_id}/containers/registries/{domain}

##### ModelsExpand Collapse

<details>

<summary>

RegistryListResponse object {created\_at, domain, kind, public\_key }

An image registry added in a customer account.

</summary>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

domain: string

A string representation of a domain name. See RFC-1034 (<a href="https://www.ietf.org/rfc/rfc1034.txt">https://www.ietf.org/rfc/rfc1034.txt</a>). Consider that the limit of a domain name is min 3 and max 253 ASCII characters.

<a href="#">Link to this property</a>

<details>

<summary>

kind: optional "ECR"or "DockerHub"or "GAR"or "default"

The type of registry that is being configured.

</summary>

One of the following:

"ECR"

<a href="#">Link to this property</a>

"DockerHub"

<a href="#">Link to this property</a>

"GAR"

<a href="#">Link to this property</a>

"default"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

public\_key: optional string

Public component of the registry credentials. For managed registries this is a base64-encoded public key; for external registries the format depends on the registry provider.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries%20%3E%20(model)%20registry_list_response%20%3E%20(schema)>)

<details>

<summary>

RegistryCreateResponse object {created\_at, domain, kind, public\_key }

An image registry added in a customer account.

</summary>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

domain: string

A string representation of a domain name. See RFC-1034 (<a href="https://www.ietf.org/rfc/rfc1034.txt">https://www.ietf.org/rfc/rfc1034.txt</a>). Consider that the limit of a domain name is min 3 and max 253 ASCII characters.

<a href="#">Link to this property</a>

<details>

<summary>

kind: optional "ECR"or "DockerHub"or "GAR"or "default"

The type of registry that is being configured.

</summary>

One of the following:

"ECR"

<a href="#">Link to this property</a>

"DockerHub"

<a href="#">Link to this property</a>

"GAR"

<a href="#">Link to this property</a>

"default"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

public\_key: optional string

Public component of the registry credentials. For managed registries this is a base64-encoded public key; for external registries the format depends on the registry provider.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries%20%3E%20(model)%20registry_create_response%20%3E%20(schema)>)

<details>

<summary>

RegistryDeleteResponse object {domain }

Result of deleting an image registry from a Containers account.

</summary>

domain: string

A string representation of a domain name. See RFC-1034 (<a href="https://www.ietf.org/rfc/rfc1034.txt">https://www.ietf.org/rfc/rfc1034.txt</a>). Consider that the limit of a domain name is min 3 and max 253 ASCII characters.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries%20%3E%20(model)%20registry_delete_response%20%3E%20(schema)>)

#### RegistriesCredentials

##### [Generate a JWT to interact with the specified image registry.](https://developers.cloudflare.com/api/resources/containers/subresources/registries/subresources/credentials/methods/generate)

POST/accounts/{account\_id}/containers/registries/{domain}/credentials

##### ModelsExpand Collapse

<details>

<summary>

CredentialGenerateResponse object {account\_id, password, registry\_host, username }

Credentials returned for an authenticated registry configured on a Containers account.

</summary>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

password: string

The password to use when authenticating to the image registry.

<a href="#">Link to this property</a>

registry\_host: string

The domain of the image registry these credentials target.

<a href="#">Link to this property</a>

username: string

The username to use when authenticating to the image registry.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries.credentials%20%3E%20(model)%20credential_generate_response%20%3E%20(schema)>)