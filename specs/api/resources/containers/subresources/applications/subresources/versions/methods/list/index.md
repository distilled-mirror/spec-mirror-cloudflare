---
title: List all application versions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

[Versions](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/versions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List all application versions

GET/accounts/{account\_id}/containers/applications/{application\_id}/versions

Returns all versions for a scheduler-backed application with `scheduling_policy: "default"`. Versions and rollouts do not apply to applications with `scheduling_policy: "durable_object"`.

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

`Workers Containers Write``Workers Containers Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

application\_id: string

An Application ID represents an identifier of an application.

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20application_id%20%3E%20(schema)>)

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

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {configuration, percentage, version }

</summary>

<details>

<summary>

configuration: object {authorized\_keys, command, entrypoint, 4 more }

User-specified container configuration changes.

</summary>

<details>

<summary>

authorized\_keys: optional array of object {public\_key, name }

</summary>

public\_key: string

An SSH public key.

<a href="#">Link to this property</a>

name: optional string

Optional human readable name for this key.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

command: optional array of string

The command that runs when the container starts, passed to the entrypoint. You can override this at run-time. If you override only the command, it gets passed to the default entrypoint specified in the image.

<a href="#">Link to this property</a>

entrypoint: optional array of string

The entry point for the container, specifying the executable to run when the container starts. You can override this at run-time. If you do, the default command from the image is ignored. Specify both entrypoint and command at run-time to completely replace the image defaults.

<a href="#">Link to this property</a>

<details>

<summary>

environment\_variables: optional array of object {name, value }

Container environment variables.

</summary>

name: string

An environment variable name.

<a href="#">Link to this property</a>

value: string

An environment variable value.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

image: optional string

Image url.

<a href="#">Link to this property</a>

<details>

<summary>

instance\_type: optional "lite"or "basic"or "standard-1"or 3 more

The instance type configures vCPU, memory, and disk.

- “lite”: 1/16 vCPU, 256 MiB memory, 2 GB disk
- “basic”: 1/4 vCPU, 1 GiB memory, 4 GB disk
- “standard-1”: 1/2 vCPU, 4 GiB memory, 8 GB disk
- “standard-2”: 1 vCPU, 6 GiB memory, 12 GB disk
- “standard-3”: 2 vCPU, 8 GiB memory, 16 GB disk
- “standard-4”: 4 vCPU, 12 GiB memory, 20 GB disk

</summary>

One of the following:

"lite"

<a href="#">Link to this property</a>

"basic"

<a href="#">Link to this property</a>

"standard-1"

<a href="#">Link to this property</a>

"standard-2"

<a href="#">Link to this property</a>

"standard-3"

<a href="#">Link to this property</a>

"standard-4"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Settings for deployment observability such as logging.

</summary>

<details>

<summary>

logs: optional object {enabled }

Observability logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

percentage: number

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.applications.versions%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List all application versions

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/applications/$APPLICATION_ID/versions \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
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
  "result": [
    {
      "configuration": {
        "authorized_keys": [
          {
            "public_key": "public_key",
            "name": "name"
          }
        ],
        "command": [
          "myapp",
          "--default-option"
        ],
        "entrypoint": [
          "/bin/bash"
        ],
        "environment_variables": [
          {
            "name": "name",
            "value": "value"
          }
        ],
        "image": "image",
        "instance_type": "lite",
        "observability": {
          "logs": {
            "enabled": true
          }
        }
      },
      "percentage": 0,
      "version": 0
    }
  ],
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
  "result": [
    {
      "configuration": {
        "authorized_keys": [
          {
            "public_key": "public_key",
            "name": "name"
          }
        ],
        "command": [
          "myapp",
          "--default-option"
        ],
        "entrypoint": [
          "/bin/bash"
        ],
        "environment_variables": [
          {
            "name": "name",
            "value": "value"
          }
        ],
        "image": "image",
        "instance_type": "lite",
        "observability": {
          "logs": {
            "enabled": true
          }
        }
      },
      "percentage": 0,
      "version": 0
    }
  ],
  "success": true
}
```