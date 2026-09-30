---
title: Credentials
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Registries](https://developers.cloudflare.com/api/resources/containers/subresources/registries)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Credentials

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