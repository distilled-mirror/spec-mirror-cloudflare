---
title: Generate a JWT to interact with the specified image registry.
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Registries](https://developers.cloudflare.com/api/resources/containers/subresources/registries)

[Credentials](https://developers.cloudflare.com/api/resources/containers/subresources/registries/subresources/credentials)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Generate a JWT to interact with the specified image registry.

POST/accounts/{account\_id}/containers/registries/{domain}/credentials

Generates credentials for accessing a configured container image registry.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

domain: string

The domain to get credentials for.

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(params)%20default%20%3E%20(param)%20domain%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

expiration\_minutes: optional number

The number of minutes Cloudflare managed registry credentials stay valid. Required for managed registries and must remain positive. Cloudflare ignores this value for external registries.

minimum1

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(params)%200%20%3E%20(param)%20expiration_minutes%20%3E%20(schema)>)

<details>

<summary>

permissions: optional array of "pull"or "push"or "list"

The permissions for Cloudflare managed registry credentials. Required for managed registries. Cloudflare ignores this value for external registries.

</summary>

One of the following:

"pull"

<a href="#">Link to this property</a>

"push"

<a href="#">Link to this property</a>

"list"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(params)%200%20%3E%20(param)%20permissions%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {account\_id, password, registry\_host, username }

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

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.registries.credentials%20%3E%20(method)%20generate%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Generate a JWT to interact with the specified image registry.

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/registries/$DOMAIN/credentials \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{}'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "account_id": "account_id",
    "password": "password",
    "registry_host": "registry_host",
    "username": "username"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "account_id": "account_id",
    "password": "password",
    "registry_host": "registry_host",
    "username": "username"
  },
  "success": true
}
```