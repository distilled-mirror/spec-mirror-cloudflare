---
title: Get a container instance
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

[Instances](https://developers.cloudflare.com/api/resources/containers/subresources/applications/subresources/instances)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a container instance

GET/accounts/{account\_id}/containers/applications/{application\_id}/instances/{instance\_id}

Returns a container instance belonging to an application.

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

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

application\_id: string

An Application ID represents an identifier of an application.

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20application_id%20%3E%20(schema)>)

instance\_id: string

A container instance ID (64-character hex Durable Object actor ID).

maxLength64

minLength64

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20instance_id%20%3E%20(schema)>)

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

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, application\_id, image, 5 more }

The last-reported state of a logical container instance.

</summary>

id: string

A container instance ID (64-character hex Durable Object actor ID).

maxLength64

minLength64

<a href="#">Link to this property</a>

application\_id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

image: string

The image for the current container placement, when one is available.

<a href="#">Link to this property</a>

<details>

<summary>

status: object {state, updated\_at, exit\_code }

The latest known status of a container instance.

</summary>

<details>

<summary>

state: "provisioning"or "running"or "failed"or 5 more

The current lifecycle state of a container instance.

</summary>

One of the following:

"provisioning"

<a href="#">Link to this property</a>

"running"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"stopping"

<a href="#">Link to this property</a>

"stopped"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"inactive"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

exit\_code: optional number

The process exit code, when the runtime reports one.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {disk, memory, vcpu }

The resources allocated to the container instance.

</summary>

disk: number

Disk allocated to the container instance, in decimal MB.

minimum1

<a href="#">Link to this property</a>

memory: number

Memory allocated to the container instance, in MiB.

minimum1

<a href="#">Link to this property</a>

vcpu: number

Number of virtual CPUs allocated to the container instance.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {name, region }

The location of the instance’s current container placement.

</summary>

name: string

Unique location code used to identify locations on a logical level.

<a href="#">Link to this property</a>

region: string

Represents a group of datacenters. Choose one of “AFR”, “APAC”, “EEUR”, “ENAM”, “WNAM”, “ME”, “OC”, “SAM”, or “WEUR”.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The customer-provided instance name, when available. Its UTF-8 encoding uses at most 1,024 bytes.

<a href="#">Link to this property</a>

started\_at: optional string

The time at which the current container placement started, when one exists.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.applications.instances%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get a container instance

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/applications/$APPLICATION_ID/instances/$INSTANCE_ID \
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
  "result": {
    "id": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    "application_id": "application_id",
    "image": "image",
    "status": {
      "state": "provisioning",
      "updated_at": "2021-04-01T12:32:41.488Z",
      "exit_code": 0
    },
    "configuration": {
      "disk": 1,
      "memory": 1,
      "vcpu": 1
    },
    "location": {
      "name": "name",
      "region": "WNAM"
    },
    "name": "name",
    "started_at": "2021-04-01T12:32:41.488Z"
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
    "id": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    "application_id": "application_id",
    "image": "image",
    "status": {
      "state": "provisioning",
      "updated_at": "2021-04-01T12:32:41.488Z",
      "exit_code": 0
    },
    "configuration": {
      "disk": 1,
      "memory": 1,
      "vcpu": 1
    },
    "location": {
      "name": "name",
      "region": "WNAM"
    },
    "name": "name",
    "started_at": "2021-04-01T12:32:41.488Z"
  },
  "success": true
}
```