---
title: List tenant accounts
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Tenants](https://developers.cloudflare.com/api/resources/tenants)

[Accounts](https://developers.cloudflare.com/api/resources/tenants/subresources/accounts)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List tenant accounts

GET/tenants/{tenant\_id}/accounts

Lists the Cloudflare accounts associated with this tenant using the legacy Account response shape. Use `GET /organizations/{organization_id}/accounts` for the modern Account response. Use `page_token` and `page_size` for cursor pagination, or provide `page` and `per_page` together for legacy offset pagination. Cursor pagination takes precedence when requested.

##### Security

API Email + API Key

The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**`X-Auth-Email: user@example.com`

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**`X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194`

##### P ath ParametersExpand Collapse

tenant\_id: string

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tenant_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

account\_pubname: optional object {contains, endsWith, startsWith }

</summary>

contains: optional string

(case-insensitive) Filter the list of accounts to where the account\_pubname contains a particular string.

<a href="#">Link to this property</a>

endsWith: optional string

(case-insensitive) Filter the list of accounts to where the account\_pubname ends with a particular string.

<a href="#">Link to this property</a>

startsWith: optional string

(case-insensitive) Filter the list of accounts to where the account\_pubname starts with a particular string.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_pubname%20%3E%20(schema)>)

<details>

<summary>

direction: optional "asc"or "desc"

Sort direction for the order\_by field. Valid values: <code>asc</code>, <code>desc</code>. Defaults to <code>asc</code> when order\_by is specified.

</summary>

One of the following:

"asc"

<a href="#">Link to this property</a>

"desc"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20direction%20%3E%20(schema)>)

include\_total: optional boolean

Whether to calculate and return the exact `result_info.total_size` for cursor pagination. Defaults to true. When false, `total_size` is omitted. Legacy `page`/`per_page` requests always calculate `total_count`.

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20include_total%20%3E%20(schema)>)

<details>

<summary>

name: optional object {contains, endsWith, startsWith }

</summary>

contains: optional string

(case-insensitive) Filter the list of accounts to where the name contains a particular string.

<a href="#">Link to this property</a>

endsWith: optional string

(case-insensitive) Filter the list of accounts to where the name ends with a particular string.

<a href="#">Link to this property</a>

startsWith: optional string

(case-insensitive) Filter the list of accounts to where the name starts with a particular string.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20name%20%3E%20(schema)>)

order\_by: optional "account\_name"

Field to order results by. Currently supported values: `account_name`.

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20order_by%20%3E%20(schema)>)

page: optional number

Legacy offset page number. Must be provided with `per_page`. Values below 1 are treated as

1. Cursor pagination takes precedence when requested.

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

page\_size: optional number

The amount of items to return. Defaults to 10.

maximum1000

minimum0

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page_size%20%3E%20(schema)>)

page\_token: optional string

An opaque token returned from the last list response that when provided will retrieve the next page.

Parameters used to filter the retrieved list must remain in subsequent requests with a page token.

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page_token%20%3E%20(schema)>)

per\_page: optional number

Legacy offset page size. Must be provided with `page`. Values are clamped to the range 1-100. Cursor pagination takes precedence when requested.

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

<details>

<summary>

status: optional "active"or "deleted"

Filter accounts by lifecycle status. Defaults to <code>active</code>.

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"deleted"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20status%20%3E%20(schema)>)

##### ReturnsExpand Collapse

errors: array of unknown

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

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

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {account\_pubname, account\_tag, account\_type, 2 more }

</summary>

account\_pubname: string

<a href="#">Link to this property</a>

account\_tag: string

<a href="#">Link to this property</a>

<details>

<summary>

account\_type: "standard"or "enterprise"

</summary>

One of the following:

"standard"

<a href="#">Link to this property</a>

"enterprise"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_on: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

settings: object {access\_approval\_expiry, api\_access\_enabled, enforce\_two\_factor, use\_account\_custom\_ns\_by\_default }

</summary>

access\_approval\_expiry: string

formatdate-time

<a href="#">Link to this property</a>

api\_access\_enabled: boolean

<a href="#">Link to this property</a>

enforce\_two\_factor: boolean

<a href="#">Link to this property</a>

use\_account\_custom\_ns\_by\_default: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {next\_page\_token, total\_size } or object {count, page, per\_page, total\_count }

</summary>

One of the following:

<details>

<summary>

OrganizationsAPIPageTokenResultInfo object {next\_page\_token, total\_size }

</summary>

next\_page\_token: optional string

Use this opaque token in the next request to retrieve the next page.

Parameters used to filter the retrieved list must remain in subsequent requests with a page token.

<a href="#">Link to this property</a>

total\_size: optional number

Counts the total amount of items in a list with the applied filters. The API omits next\_page\_token to indicate no more items in a particular list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OrganizationsAPILegacyPaginationResultInfo object {count, page, per\_page, total\_count }

</summary>

count: number

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

[Link to this property](#)%20tenants.accounts%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List tenant accounts

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/tenants/$TENANT_ID/accounts \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
```

200 example

```
{
  "errors": [],
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
      "account_pubname": "account_pubname",
      "account_tag": "account_tag",
      "account_type": "standard",
      "created_on": "2019-12-27T18:11:19.117Z",
      "settings": {
        "access_approval_expiry": "2019-12-27T18:11:19.117Z",
        "api_access_enabled": true,
        "enforce_two_factor": true,
        "use_account_custom_ns_by_default": true
      }
    }
  ],
  "result_info": {
    "next_page_token": "next_page_token",
    "total_size": 0
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [],
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
      "account_pubname": "account_pubname",
      "account_tag": "account_tag",
      "account_type": "standard",
      "created_on": "2019-12-27T18:11:19.117Z",
      "settings": {
        "access_approval_expiry": "2019-12-27T18:11:19.117Z",
        "api_access_enabled": true,
        "enforce_two_factor": true,
        "use_account_custom_ns_by_default": true
      }
    }
  ],
  "result_info": {
    "next_page_token": "next_page_token",
    "total_size": 0
  },
  "success": true
}
```