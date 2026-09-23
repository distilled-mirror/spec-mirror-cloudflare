---
title: List Worker Deployments
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Scripts](https://developers.cloudflare.com/api/resources/workers/subresources/scripts)

[Deployments](https://developers.cloudflare.com/api/resources/workers/subresources/scripts/subresources/deployments)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Worker Deployments

GET/accounts/{account\_id}/workers/scripts/{script\_name}/deployments

List Worker deployments. The first deployment in the list is the latest deployment actively serving traffic.

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

`Workers Tail Read``Workers Scripts Write``Workers Scripts Read`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

script\_name: string

Name of the script, used in URLs and route configuration.

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20script_name%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

page: optional number

Current page.

minimum1

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

Items per page.

maximum100

minimum1

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

since: optional string

Start of the deployment creation time range, inclusive.

formatdate-time

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20since%20%3E%20(schema)>)

until: optional string

End of the deployment creation time range, inclusive.

formatdate-time

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20until%20%3E%20(schema)>)

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

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {deployments }

</summary>

<details>

<summary>

deployments: array of <a href="https://developers.cloudflare.com/api/resources/workers#(resource)%20workers.scripts.deployments%20%3E%20(model)%20deployment%20%3E%20(schema)">Deployment</a> { id, created\_on, source, 4 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

created\_on: string

formatdate-time

<a href="#">Link to this property</a>

source: string

<a href="#">Link to this property</a>

strategy: "percentage"

<a href="#">Link to this property</a>

<details>

<summary>

versions: array of object {percentage, version\_id }

Worker versions included in this deployment. Each object must contain a <code>version_id</code> UUID and a <code>percentage</code>; percentages across all objects must total 100. In the <code>cf</code> CLI, pass the entire array as one JSON value to <code>--versions</code>, either inline, for example <code>--versions '[{"version_id":"023e105f-2a42-4f8b-a1c1-73f6a2a30c0f","percentage":100}]'</code>, or from a JSON file with <code>--versions @versions.json</code>.

</summary>

percentage: number

Percentage of traffic served by this version.

maximum100

minimum0.01

<a href="#">Link to this property</a>

version\_id: string

Identifier of the Worker Version.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

annotations: optional object {"workers/message", "workers/triggered\_by" }

</summary>

"workers/message": optional string

Human-readable message about the deployment. Truncated to 1000 bytes if longer.

maxLength1000

<a href="#">Link to this property</a>

"workers/triggered\_by": optional string

Operation that triggered the creation of the deployment.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

author\_email: optional string

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result\_info: optional object {count, page, per\_page, 2 more }

</summary>

count: optional number

Total number of results for the requested service.

<a href="#">Link to this property</a>

page: optional number

Current page within paginated list of results.

<a href="#">Link to this property</a>

per\_page: optional number

Number of results per page of results.

<a href="#">Link to this property</a>

total\_count: optional number

Total results available without any search parameters.

<a href="#">Link to this property</a>

total\_pages: optional number

The number of total pages in the entire result set.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.scripts.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### List Worker Deployments

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/scripts/$SCRIPT_NAME/deployments \
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
    "deployments": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "created_on": "2019-12-27T18:11:19.117Z",
        "source": "api",
        "strategy": "percentage",
        "versions": [
          {
            "percentage": 100,
            "version_id": "023e105f-2a42-4f8b-a1c1-73f6a2a30c0f"
          }
        ],
        "annotations": {
          "workers/message": "Deploy bug fix.",
          "workers/triggered_by": "deployment"
        },
        "author_email": "dev@stainless.com"
      }
    ]
  },
  "success": true,
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
  }
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
    "deployments": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "created_on": "2019-12-27T18:11:19.117Z",
        "source": "api",
        "strategy": "percentage",
        "versions": [
          {
            "percentage": 100,
            "version_id": "023e105f-2a42-4f8b-a1c1-73f6a2a30c0f"
          }
        ],
        "annotations": {
          "workers/message": "Deploy bug fix.",
          "workers/triggered_by": "deployment"
        },
        "author_email": "dev@stainless.com"
      }
    ]
  },
  "success": true,
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
  }
}
```