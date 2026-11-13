---
title: Select region
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Account Regions](https://developers.cloudflare.com/api/resources/zero_trust/subresources/regions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Select region

PUT/accounts/{account\_id}/zerotrust/region

Selects the region that the account uses for Cloudflare One. The region must be one of the account’s available regions. Selecting the active region again has no effect.

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

Cloudflare account ID

maxLength32

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

region\_key: string

The key of a Data Localization Suite region.

minLength1

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20region_key%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, context }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

context: optional map\[unknown]

Optional error-specific context.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, context }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

context: optional map\[unknown]

Optional error-specific context.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.regions%20%3E%20(model)%20active_account_region%20%3E%20(schema)">ActiveAccountRegion</a> { region\_key }

</summary>

region\_key: string

The key of the account’s active Data Localization Suite region, or <code>null</code> if the account has not selected a region.

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful

[Link to this property](#)%20zero_trust.regions%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Select region

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/zerotrust/region \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "region_key": "eu"
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "context": {
        "foo": "bar"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "context": {
        "foo": "bar"
      }
    }
  ],
  "result": {
    "region_key": "eu"
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
      "context": {
        "foo": "bar"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "context": {
        "foo": "bar"
      }
    }
  ],
  "result": {
    "region_key": "eu"
  },
  "success": true
}
```