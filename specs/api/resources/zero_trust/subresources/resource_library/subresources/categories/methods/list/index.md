---
title: List application categories
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Resource Library](https://developers.cloudflare.com/api/resources/zero_trust/subresources/resource_library)

[Categories](https://developers.cloudflare.com/api/resources/zero_trust/subresources/resource_library/subresources/categories)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List application categories

GET/accounts/{account\_id}/resource-library/categories

List the categories available for classifying applications, ordered by name. Results are paginated by `offset` or `cursor`.

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

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Opaque value from `result_info.cursor` of the previous response. Returns the categories that follow it. `limit` may change between requests. An empty value is the same as no cursor. A modified cursor, or one returned by a different list, returns `400`.

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

limit: optional number

Number of results to return. Defaults to 25; values are clamped to 1–250.

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

offset: optional number

Number of results to skip. Defaults to 0; negative values are clamped to 0. Ignored when `cursor` is provided.

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20offset%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Indicates whether the API call was successful.

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional array of object {id, created\_at, description, name }

Returns the list of categories.

</summary>

id: number

Numeric identifier for an application category.

formatint64

maximum4294967295

minimum1

<a href="#">Link to this property</a>

created\_at: string

Returns the category creation time.

<a href="#">Link to this property</a>

description: string

Returns the category description.

<a href="#">Link to this property</a>

name: string

Returns the category name.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: optional object {count, cursor, page, 3 more }

</summary>

count: optional number

Returns the number of results in this response.

<a href="#">Link to this property</a>

cursor: optional string

Returns an opaque cursor for the next page when more results follow. Send it as the <code>cursor</code> query parameter. Omitted on the last page.

<a href="#">Link to this property</a>

page: optional number

Returns the zero-based result offset, not a page number. Returns 0 when the request used a cursor.

<a href="#">Link to this property</a>

per\_page: optional number

Returns the effective <code>limit</code> for this response.

<a href="#">Link to this property</a>

total\_count: optional number

Returns the number of results matching the request before pagination.

<a href="#">Link to this property</a>

total\_pages: optional number

Returns the number of pages at the effective <code>limit</code>, including 0 when there are no matches.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.resource_library.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### List application categories

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/resource-library/categories \
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
  "success": true,
  "result": [
    {
      "id": 12,
      "created_at": "2025-01-01T00:00:00Z",
      "description": "Category description",
      "name": "Category name"
    }
  ],
  "result_info": {
    "count": 10,
    "cursor": "cursor",
    "page": 0,
    "per_page": 25,
    "total_count": 2000,
    "total_pages": 80
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
  "success": true,
  "result": [
    {
      "id": 12,
      "created_at": "2025-01-01T00:00:00Z",
      "description": "Category description",
      "name": "Category name"
    }
  ],
  "result_info": {
    "count": 10,
    "cursor": "cursor",
    "page": 0,
    "per_page": 25,
    "total_count": 2000,
    "total_pages": 80
  }
}
```