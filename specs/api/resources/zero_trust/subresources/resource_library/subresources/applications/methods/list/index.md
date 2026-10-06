---
title: List applications
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Resource Library](https://developers.cloudflare.com/api/resources/zero_trust/subresources/resource_library)

[Applications](https://developers.cloudflare.com/api/resources/zero_trust/subresources/resource_library/subresources/applications)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List applications

GET/accounts/{account\_id}/resource-library/applications

List the applications available to an account, both the applications Cloudflare curates and the custom applications the account has defined.

Results are paginated. Use `filter` and `search` to narrow the list, `order_by` to sort it, and `fields` to reduce each result to only the properties you need. Use `lookup` to find complete application names mentioned in a rule sentence, ignoring case. Lookup does not correct misspellings. It ranks matches by relevance and uses the same filters, fields, and pagination as listing. `lookup` cannot be combined with `search`.

The authenticated principal must have access to the account identified by `account_id`.

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

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

fields: optional string

Return only the listed properties on each application, as a comma-separated list. Use this to keep responses small when you only need part of each application, for example populating a picker with `fields=id,name` instead of downloading every hostname and IP subnet.

Omit this parameter to receive the full application object, including when lookup is used.

`id` is always returned.

Selectable properties: `id`, `name`, `human_id`, `version`, `hostnames`, `support_domains`, `ip_subnets`, `port_protocols`, `supported`, `gen_ai_score`, `application_confidence_score`, `created_at`, `updated_at`, `review_status`.

Unknown or empty property names return `400`.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20fields%20%3E%20(schema)>)

filter: optional string

Filter applications using `key:value` format. Supported filter keys:

- `name`: application name (for example, `name:HR`).
- `id`: application ID (for example, `id:498`).
- `human_id`: human-readable ID (for example, `human_id:HR`).
- `hostname`: hostname or support domain (for example, `hostname:portal.example.com`).
- `source`: application source name (for example, `source:cloudflare`).
- `ip_subnet`: CIDR containment; returns applications where a stored subnet contains the search value (for example, `ip_subnet:10.0.1.5/32` matches `10.0.0.0/16`).
- `category_id`: category ID (for example, `category_id:12`).
- `category_name`: category name (for example, `category_name:HR`).
- `supported`: supported Cloudflare product. Values: `GATEWAY`, `ACCESS`, `CASB`.
- `review_status`: account-specific Gateway review status. Values: `approved`, `unapproved`, `in_review`, `unreviewed`.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20filter%20%3E%20(schema)>)

limit: optional number

Number of results to return. Defaults to 25; values are clamped to 1–250.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

lookup: optional string

Find complete, case-insensitive application name mentions in a phrase or rule sentence. Misspelled names do not match. Returns matching applications ranked by relevance. Must be between 2 and 1000 characters. Uses the same filters, fields, and pagination as listing. `search` cannot be combined with lookup. Results are ranked by relevance, so `order_by` is ignored.

maxLength1000

minLength2

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20lookup%20%3E%20(schema)>)

offset: optional number

Number of results to skip. Defaults to 0; negative values are clamped to 0.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20offset%20%3E%20(schema)>)

order\_by: optional string

Order results using field:direction format. Supported fields are name, id, human\_id, category\_id, application\_type, application\_confidence\_score, and gen\_ai\_score. Supported directions are asc and desc. Ignored when search is provided; results are ranked by relevance instead. Also ignored when lookup is provided.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20order_by%20%3E%20(schema)>)

search: optional string

Fuzzy search across application name and hostnames. Results are ranked by relevance. Must be between 2 and 200 characters. Can be combined with filter parameters.

maxLength200

minLength2

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20search%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Indicates whether the API call was successful.

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional array of object {id, application\_confidence\_score, application\_score\_composition, 16 more }

Returns the list of applications.

</summary>

id: number

Numeric identifier for the application.

formatint64

maximum4294967295

minimum0

<a href="#">Link to this property</a>

application\_confidence\_score: optional number

Confidence score for the application. Returns -1 when no score is available.

formatfloat

<a href="#">Link to this property</a>

application\_score\_composition: optional unknown

Returns the score composition breakdown for the application.

<a href="#">Link to this property</a>

application\_source: optional string

Returns the application source.

<a href="#">Link to this property</a>

application\_type: optional string

Returns the application type.

<a href="#">Link to this property</a>

application\_type\_description: optional string

Returns the application type description.

<a href="#">Link to this property</a>

category\_id: optional number

Numeric identifier for an application category.

formatint64

maximum4294967295

minimum1

<a href="#">Link to this property</a>

created\_at: optional string

Returns the application creation time.

<a href="#">Link to this property</a>

gen\_ai\_score: optional number

GenAI score for the application. Returns -1 when no score is available.

formatfloat

<a href="#">Link to this property</a>

hostnames: optional array of string

Hostnames matched by the application.

<a href="#">Link to this property</a>

human\_id: optional string

Human-readable identifier for the application.

<a href="#">Link to this property</a>

ip\_subnets: optional array of string

IP subnets for this application. Custom application create and update requests accept IPv4 prefix lengths /8 through /32 and IPv6 prefix lengths /32 through /128.

<a href="#">Link to this property</a>

name: optional string

Application name.

<a href="#">Link to this property</a>

port\_protocols: optional array of string

Ports matched by the application, in <code>protocol/port</code> or inclusive <code>protocol/start-end</code> format (for example, <code>tcp/443</code> or <code>udp/10000-20000</code>). TCP and UDP ports must be between 0 and 65535.

<a href="#">Link to this property</a>

<details>

<summary>

review\_status: optional "approved"or "unapproved"or "in\_review"or "unreviewed"

The account-specific Gateway review status. Applications with no assigned review status are returned as <code>unreviewed</code>.

</summary>

One of the following:

"approved"

<a href="#">Link to this property</a>

"unapproved"

<a href="#">Link to this property</a>

"in\_review"

<a href="#">Link to this property</a>

"unreviewed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_domains: optional array of string

Support domains matched by the application.

<a href="#">Link to this property</a>

<details>

<summary>

supported: optional array of "GATEWAY"or "ACCESS"or "CASB"

Cloudflare products that support this application.

</summary>

One of the following:

"GATEWAY"

<a href="#">Link to this property</a>

"ACCESS"

<a href="#">Link to this property</a>

"CASB"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: optional string

Returns the application update time.

<a href="#">Link to this property</a>

version: optional string

Returns the application version.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: optional object {count, page, per\_page, 2 more }

</summary>

count: optional number

Returns the number of results in this response.

<a href="#">Link to this property</a>

page: optional number

Returns the zero-based result offset, not a page number.

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

[Link to this property](#)%20zero_trust.resource_library.applications%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### List applications

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/resource-library/applications \
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
      "id": 498,
      "application_confidence_score": 0.92,
      "application_score_composition": {
        "categories": [
          {
            "confidence": 0.95,
            "name": "Security"
          }
        ],
        "plan": "free"
      },
      "application_source": "cloudflare",
      "application_type": "Human Resources",
      "application_type_description": "Applications used to manage employees and workforce tools.",
      "category_id": 12,
      "created_at": "2025-01-01T00:00:00Z",
      "gen_ai_score": 1.5,
      "hostnames": [
        "example.com",
        "foo.com"
      ],
      "human_id": "HR",
      "ip_subnets": [
        "192.168.1.0/24",
        "2001:db8::/48"
      ],
      "name": "HR",
      "port_protocols": [
        "tcp/443",
        "udp/10000-20000"
      ],
      "review_status": "approved",
      "support_domains": [
        "example.com",
        "foo.com"
      ],
      "supported": [
        "GATEWAY",
        "ACCESS"
      ],
      "updated_at": "2025-01-01T00:00:00Z",
      "version": "2025-01-01T00:00:00Z"
    }
  ],
  "result_info": {
    "count": 10,
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
      "id": 498,
      "application_confidence_score": 0.92,
      "application_score_composition": {
        "categories": [
          {
            "confidence": 0.95,
            "name": "Security"
          }
        ],
        "plan": "free"
      },
      "application_source": "cloudflare",
      "application_type": "Human Resources",
      "application_type_description": "Applications used to manage employees and workforce tools.",
      "category_id": 12,
      "created_at": "2025-01-01T00:00:00Z",
      "gen_ai_score": 1.5,
      "hostnames": [
        "example.com",
        "foo.com"
      ],
      "human_id": "HR",
      "ip_subnets": [
        "192.168.1.0/24",
        "2001:db8::/48"
      ],
      "name": "HR",
      "port_protocols": [
        "tcp/443",
        "udp/10000-20000"
      ],
      "review_status": "approved",
      "support_domains": [
        "example.com",
        "foo.com"
      ],
      "supported": [
        "GATEWAY",
        "ACCESS"
      ],
      "updated_at": "2025-01-01T00:00:00Z",
      "version": "2025-01-01T00:00:00Z"
    }
  ],
  "result_info": {
    "count": 10,
    "page": 0,
    "per_page": 25,
    "total_count": 2000,
    "total_pages": 80
  }
}
```