---
title: Get a user population user
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[User Populations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations)

[Users](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a user population user

GET/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

Fetches a SCIM user from a user population.

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

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

user\_population\_id: string

UUID.

maxLength36

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20user_population_id%20%3E%20(schema)>)

user\_id: string

The SCIM user identifier.

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20user_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

attributes: optional string

Comma-separated SCIM attributes to return.

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20attributes%20%3E%20(schema)>)

excludedAttributes: optional string

Comma-separated SCIM attributes to exclude from the response.

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20excludedAttributes%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {id, active, displayName, 6 more }

A SCIM User resource. Additional SCIM extension attributes are supported.

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Get a user population user

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/user_populations/$USER_POPULATION_ID/users/$USER_ID \
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
  "result": {
    "id": "id",
    "active": true,
    "displayName": "displayName",
    "emails": [
      {
        "primary": true,
        "type": "type",
        "value": "value"
      }
    ],
    "externalId": "externalId",
    "meta": {
      "created": "2019-12-27T18:11:19.117Z",
      "lastModified": "2019-12-27T18:11:19.117Z",
      "location": "https://example.com",
      "resourceType": "resourceType",
      "version": "version"
    },
    "name": {
      "familyName": "familyName",
      "formatted": "formatted",
      "givenName": "givenName",
      "honorificPrefix": "honorificPrefix",
      "honorificSuffix": "honorificSuffix",
      "middleName": "middleName"
    },
    "schemas": [
      "string"
    ],
    "userName": "userName"
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
  "result": {
    "id": "id",
    "active": true,
    "displayName": "displayName",
    "emails": [
      {
        "primary": true,
        "type": "type",
        "value": "value"
      }
    ],
    "externalId": "externalId",
    "meta": {
      "created": "2019-12-27T18:11:19.117Z",
      "lastModified": "2019-12-27T18:11:19.117Z",
      "location": "https://example.com",
      "resourceType": "resourceType",
      "version": "version"
    },
    "name": {
      "familyName": "familyName",
      "formatted": "formatted",
      "givenName": "givenName",
      "honorificPrefix": "honorificPrefix",
      "honorificSuffix": "honorificSuffix",
      "middleName": "middleName"
    },
    "schemas": [
      "string"
    ],
    "userName": "userName"
  }
}
```