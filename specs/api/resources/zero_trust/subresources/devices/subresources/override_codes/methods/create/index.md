---
agent:
  instructions: "This site offers a search API that returns relevant content across the entire site. Use the search endpoint to find information instead of crawling individual pages."
  search: "https://developers.cloudflare.com/.well-known/search?q={query}"
title: Generate an uninstall protection override code
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Devices](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices)

[Override Codes](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/override_codes)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Generate an uninstall protection override code

POST/accounts/{account\_id}/devices/override\_codes

Generates an account-wide or device-specific uninstall protection override code.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

duration\_hours: number

Number of hours for which the override code should remain valid.

maximum24

minimum1

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20duration_hours%20%3E%20(schema)>)

<details>

<summary>

scope: "account" or "device"

Whether the code applies to every device in the account or one physical device.

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"device"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20scope%20%3E%20(schema)>)

type: "uninstall\_protection"

The feature that the override code applies to.

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20type%20%3E%20(schema)>)

device\_id: optional string

Physical device ID. Required when scope is device and forbidden when scope is account.

formatuuid

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20device_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { code, message }

</summary>

code: number

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { code }

</summary>

code: string

Uninstall protection override code.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Generate an uninstall protection override code

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/devices/override_codes \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "duration_hours": 1,
          "scope": "account",
          "type": "uninstall_protection"
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "code": "code"
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
      "code": 0,
      "message": "message"
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "code": "code"
  },
  "success": true
}
```