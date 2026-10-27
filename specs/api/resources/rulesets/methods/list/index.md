---
title: List account or zone rulesets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Rulesets](https://developers.cloudflare.com/api/resources/rulesets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List account or zone rulesets

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/rulesets

Fetches all rulesets.

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

`Mass URL Redirects Write``Mass URL Redirects Read``Magic Firewall Write``Magic Firewall Read``L4 DDoS Managed Ruleset Write``L4 DDoS Managed Ruleset Read``Transform Rules Write``Transform Rules Read``Select Configuration Write``Select Configuration Read``Account WAF Write``Account WAF Read``Account Rulesets Read``Account Rulesets Write``Logs Write``Logs Read`

##### P ath ParametersExpand Collapse

account\_id: optional string

The Account ID to use for this endpoint. Mutually exclusive with the Zone ID.

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

zone\_id: optional string

The Zone ID to use for this endpoint. Mutually exclusive with the Account ID.

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

The cursor to use for the next page.

minLength1

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

per\_page: optional number

The number of rulesets to return per page.

maximum50

minimum1

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message, code, source }

A list of error messages.

</summary>

message: string

A text description of this message.

minLength1

<a href="#">Link to this property</a>

code: optional number

A unique code for this message.

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

The source of this message.

</summary>

pointer: string

A JSON pointer to the field that is the source of the message.

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code, source }

A list of warning messages.

</summary>

message: string

A text description of this message.

minLength1

<a href="#">Link to this property</a>

code: optional number

A unique code for this message.

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

The source of this message.

</summary>

pointer: string

A JSON pointer to the field that is the source of the message.

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: unknownor array of unknownor stringor 2 more

A result.

</summary>

One of the following:

unknown

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result\_info: optional object {cursors }

Information to navigate the results.

</summary>

<details>

<summary>

cursors: optional object {after }

The set of cursors.

</summary>

after: string

The cursor to use for the next page.

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20rulesets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### List account or zone rulesets

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/$ACCOUNTS_OR_ZONES/$ACCOUNT_OR_ZONE_ID/rulesets \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "message": "something bad happened",
      "code": 10000,
      "source": {
        "pointer": "/rules/0/action"
      }
    }
  ],
  "messages": [
    {
      "message": "something bad happened",
      "code": 10000,
      "source": {
        "pointer": "/rules/0/action"
      }
    }
  ],
  "result": {},
  "success": true,
  "result_info": {
    "cursors": {
      "after": "dGhpc2lzYW5leGFtcGxlCg"
    }
  }
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "message": "something bad happened",
      "code": 10000,
      "source": {
        "pointer": "/rules/0/action"
      }
    }
  ],
  "messages": [
    {
      "message": "something bad happened",
      "code": 10000,
      "source": {
        "pointer": "/rules/0/action"
      }
    }
  ],
  "result": {},
  "success": true,
  "result_info": {
    "cursors": {
      "after": "dGhpc2lzYW5leGFtcGxlCg"
    }
  }
}
```