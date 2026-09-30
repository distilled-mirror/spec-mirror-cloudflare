---
title: Configure a private external image registry
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Registries](https://developers.cloudflare.com/api/resources/containers/subresources/registries)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Configure a private external image registry

POST/accounts/{account\_id}/containers/registries

Registers credentials for a supported private external image registry so Containers can pull images from it. This endpoint does not create a registry or upload an image. Public Docker Hub images and images in the Cloudflare managed registry do not require this configuration.

Refer to [Image management](https://developers.cloudflare.com/containers/platform-details/image-management/) for supported registries and instructions for storing registry credentials.

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

##### Accepted Permissions (at least one required)

`Workers Containers Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

auth: object {private\_credential, public\_credential }

Credentials for authenticating to a private external image registry. Store the private credential in <a href="https://developers.cloudflare.com/secrets-store/">Secrets Store</a> before calling the API. Refer to <a href="https://developers.cloudflare.com/containers/platform-details/image-management/">Image management</a> for the credential required by each supported registry provider.

</summary>

<details>

<summary>

private\_credential: object {secret\_name, store\_id }

A reference to the private registry credential in Secrets Store. The referenced secret must have the <code>containers</code> scope. Raw secret values are not accepted.

</summary>

secret\_name: string

Name of the secret within the store.

maxLength255

minLength1

<a href="#">Link to this property</a>

store\_id: string

Identifier of the Secrets Store containing the secret.

maxLength32

minLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

public\_credential: string

The non-secret part of the registry credential: an AWS access key ID for ECR, a username for Docker Hub, or a service account email for Google Artifact Registry.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20auth%20%3E%20(schema)>)

domain: string

Hostname of the private registry, without a scheme or image path. Supported hostnames are `docker.io`, AWS ECR hostnames, and Google Artifact Registry `*-docker.pkg.dev` hostnames.

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20domain%20%3E%20(schema)>)

<details>

<summary>

kind: "ECR"or "DockerHub"or "GAR"

Registry provider. This must match <code>domain</code>: <code>DockerHub</code> for <code>docker.io</code>, <code>ECR</code> for AWS ECR, or <code>GAR</code> for Google Artifact Registry.

</summary>

One of the following:

"ECR"

<a href="#">Link to this property</a>

"DockerHub"

<a href="#">Link to this property</a>

"GAR"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20kind%20%3E%20(schema)>)

is\_public: optional false

Omit this field or set it to `false`. Public Docker Hub images do not require registry configuration and cannot be added with this endpoint.

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20is_public%20%3E%20(schema)>)

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

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {created\_at, domain, kind, public\_key }

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

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.registries%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Configure a private external image registry

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/registries \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "auth": {
            "private_credential": {
              "secret_name": "API_KEY",
              "store_id": "14758f1afd44c09b7992073ccf00b43d"
            },
            "public_credential": "example-user"
          },
          "domain": "docker.io",
          "kind": "ECR"
        }'
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
    "created_at": "2021-04-01T12:32:41.488Z",
    "domain": "docker.io",
    "kind": "ECR",
    "public_key": "public_key"
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
    "created_at": "2021-04-01T12:32:41.488Z",
    "domain": "docker.io",
    "kind": "ECR",
    "public_key": "public_key"
  },
  "success": true
}
```