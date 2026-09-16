---
title: Get Zone Entitlements
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zones](https://developers.cloudflare.com/api/resources/zones)

[Entitlements](https://developers.cloudflare.com/api/resources/zones/subresources/entitlements)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get Zone Entitlements

GET/zones/{zone\_id}/entitlements

Returns the list of entitlements (features and their allocations) for a given zone. Each entitlement describes a product feature the zone is permitted to use and the allocation value (boolean, count, range, enum, or string) that governs its behaviour.

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

`Zone Read`

##### P ath ParametersExpand Collapse

zone\_id: string

Identifier tag.

maxLength32

minLength32

[Link to this property](#)%20zones.entitlements%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message }

List of errors, empty on success.

</summary>

code: number

Numeric error code.

<a href="#">Link to this property</a>

message: string

Human-readable error message.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.entitlements%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message }

List of informational messages.

</summary>

code: number

Numeric message code.

<a href="#">Link to this property</a>

message: string

Human-readable message.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.entitlements%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, allocation, created\_date, 3 more }

List of entitlements for the requested object.

</summary>

id: string

Entitlement identifier — equal to the feature key.

<a href="#">Link to this property</a>

<details>

<summary>

allocation: object {type, value }

Represents the allocation value for an entitlement. The shape of <code>value</code> depends on <code>type</code>: <code>bool</code> uses a boolean, <code>max_count</code> uses an integer, <code>enum_number</code> uses an array of numbers, <code>range</code> uses an object with <code>min</code> and <code>max</code> integer fields, and <code>string</code> uses a string.

</summary>

<details>

<summary>

type: "bool"or "max\_count"or "enum\_number"or 2 more

Allocation type discriminator.

</summary>

One of the following:

"bool"

<a href="#">Link to this property</a>

"max\_count"

<a href="#">Link to this property</a>

"enum\_number"

<a href="#">Link to this property</a>

"range"

<a href="#">Link to this property</a>

"string"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

Contains the allocation value whose concrete type the <code>type</code> field determines: bool yields a boolean, max\_count yields an integer, enum\_number yields an array of numbers, range yields an object with <code>min</code> and <code>max</code>, and string yields a string.

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

array of number

<a href="#">Link to this property</a>

<details>

<summary>

object {max, min }

</summary>

max: number

<a href="#">Link to this property</a>

min: number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_date: string

ISO 8601 timestamp (microsecond precision, no timezone offset) when the entitlement was created. Format: <code>YYYY-MM-DDTHH:MM:SS.ffffff</code>.

<a href="#">Link to this property</a>

deleted\_date: string

ISO 8601 timestamp when the entitlement was deleted, or empty string if not deleted.

<a href="#">Link to this property</a>

edited\_date: string

ISO 8601 timestamp (microsecond precision, no timezone offset) when the entitlement was last edited.

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {id, feature\_set, key, name }

Describes a product feature associated with an entitlement.

</summary>

id: number

Numeric identifier of the feature.

formatint64

<a href="#">Link to this property</a>

feature\_set: string

The logical grouping (set) this feature belongs to.

<a href="#">Link to this property</a>

key: string

Unique string key for the feature.

<a href="#">Link to this property</a>

name: string

Human-readable name of the feature.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.entitlements%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zones.entitlements%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get Zone Entitlements

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/entitlements \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

400 example

404 example

405 example

500 example

503 example

```
{
  "errors": [],
  "messages": [],
  "result": [
    {
      "allocation": {
        "type": "max_count",
        "value": 3
      },
      "created_date": "2021-09-17T20:33:36.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:34:01.000000",
      "feature": {
        "feature_set": "page_rules",
        "id": 1,
        "key": "page_rules",
        "name": "Page Rules"
      },
      "id": "page_rules"
    },
    {
      "allocation": {
        "type": "bool",
        "value": true
      },
      "created_date": "2021-09-17T20:39:02.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:39:11.000000",
      "feature": {
        "feature_set": "argo",
        "id": 38,
        "key": "argo.allow_tiered_caching",
        "name": "Argo Tiered Cache"
      },
      "id": "argo.allow_tiered_caching"
    },
    {
      "allocation": {
        "type": "enum_number",
        "value": [
          10,
          60,
          600,
          3600
        ]
      },
      "created_date": "2021-09-17T20:47:36.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:47:43.000000",
      "feature": {
        "feature_set": "rate_limiting",
        "id": 32,
        "key": "rate_limiting.sampling_period_secs",
        "name": "rate_limiting.sampling_period_secs"
      },
      "id": "rate_limiting.sampling_period_secs"
    }
  ],
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 2005,
      "message": "failed to fetch entitlements: invalid object type"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2004,
      "message": "failed to fetch entitlements: unknown route"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "failed to fetch entitlements: method not allowed"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2000,
      "message": "failed to fetch entitlements: internal server error"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2003,
      "message": "failed to fetch entitlements: timeout occurred"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

##### Returns Examples

200 example

400 example

404 example

405 example

500 example

503 example

```
{
  "errors": [],
  "messages": [],
  "result": [
    {
      "allocation": {
        "type": "max_count",
        "value": 3
      },
      "created_date": "2021-09-17T20:33:36.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:34:01.000000",
      "feature": {
        "feature_set": "page_rules",
        "id": 1,
        "key": "page_rules",
        "name": "Page Rules"
      },
      "id": "page_rules"
    },
    {
      "allocation": {
        "type": "bool",
        "value": true
      },
      "created_date": "2021-09-17T20:39:02.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:39:11.000000",
      "feature": {
        "feature_set": "argo",
        "id": 38,
        "key": "argo.allow_tiered_caching",
        "name": "Argo Tiered Cache"
      },
      "id": "argo.allow_tiered_caching"
    },
    {
      "allocation": {
        "type": "enum_number",
        "value": [
          10,
          60,
          600,
          3600
        ]
      },
      "created_date": "2021-09-17T20:47:36.000000",
      "deleted_date": "",
      "edited_date": "2021-09-17T20:47:43.000000",
      "feature": {
        "feature_set": "rate_limiting",
        "id": 32,
        "key": "rate_limiting.sampling_period_secs",
        "name": "rate_limiting.sampling_period_secs"
      },
      "id": "rate_limiting.sampling_period_secs"
    }
  ],
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 2005,
      "message": "failed to fetch entitlements: invalid object type"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2004,
      "message": "failed to fetch entitlements: unknown route"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "failed to fetch entitlements: method not allowed"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2000,
      "message": "failed to fetch entitlements: internal server error"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 2003,
      "message": "failed to fetch entitlements: timeout occurred"
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```