---
title: Get live account usage
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get live account usage

GET/accounts/{account\_id}/containers/usage

Get current live resource usage and maximum limits for your account. Usage includes active and assigned instances.

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

[Link to this property](#)%20containers%20%3E%20(method)%20usage%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

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

[Link to this property](#)%20containers%20%3E%20(method)%20usage%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20containers%20%3E%20(method)%20usage%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {maximum, usage, utilization }

Current live usage, maximum limits, and utilization percentages for your account. Usage includes active and assigned instances and is a current snapshot, not a historical or billable metric.

</summary>

<details>

<summary>

maximum: object {disk\_mb, memory\_mib, vcpus }

Lists account limits for the resources reported in usage.

</summary>

disk\_mb: number

Maximum disk in MB for the account.

<a href="#">Link to this property</a>

memory\_mib: number

Maximum memory in MiB for the account.

<a href="#">Link to this property</a>

vcpus: number

Maximum vCPU for the account.

formatfloat

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

usage: object {disk\_mb, instances, memory\_mib, vcpus }

Lists current resource consumption for active and assigned instances.

</summary>

disk\_mb: number

<a href="#">Link to this property</a>

instances: number

<a href="#">Link to this property</a>

memory\_mib: number

<a href="#">Link to this property</a>

vcpus: number

formatfloat

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

utilization: object {disk\_mb, memory\_mib, vcpus }

Live resource utilization percentages. A value of 100 represents full utilization. Values can exceed 100 when usage exceeds quota. The API omits fields whose corresponding maximum is zero.

</summary>

disk\_mb: optional number

Live disk usage as a percentage of maximum disk.

formatfloat

<a href="#">Link to this property</a>

memory\_mib: optional number

Live memory usage as a percentage of maximum memory.

formatfloat

<a href="#">Link to this property</a>

vcpus: optional number

Live vCPU usage as a percentage of maximum vCPU.

formatfloat

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers%20%3E%20(method)%20usage%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers%20%3E%20(method)%20usage%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get live account usage

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/usage \
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
    "maximum": {
      "disk_mb": 0,
      "memory_mib": 0,
      "vcpus": 0
    },
    "usage": {
      "disk_mb": 0,
      "instances": 0,
      "memory_mib": 0,
      "vcpus": 0
    },
    "utilization": {
      "disk_mb": 0,
      "memory_mib": 0,
      "vcpus": 0
    }
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
    "maximum": {
      "disk_mb": 0,
      "memory_mib": 0,
      "vcpus": 0
    },
    "usage": {
      "disk_mb": 0,
      "instances": 0,
      "memory_mib": 0,
      "vcpus": 0
    },
    "utilization": {
      "disk_mb": 0,
      "memory_mib": 0,
      "vcpus": 0
    }
  },
  "success": true
}
```