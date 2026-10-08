---
title: List payment rules
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Monetization](https://developers.cloudflare.com/api/resources/monetization)

[Rules](https://developers.cloudflare.com/api/resources/monetization/subresources/rules)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List payment rules

GET/zones/{zone\_id}/monetization/rules

Returns the currently deployed Payment Required rules for a zone. A zone with no Payment Required ruleset returns 404.

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

zone\_id: string

The unique ID of the zone.

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message }

</summary>

code: optional number

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message }

</summary>

code: optional number

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/monetization#(resource)%20monetization.rules%20%3E%20(model)%20monetization_rule_collection%20%3E%20(schema)">MonetizationRuleCollection</a> { rules }

The zone’s payment rules. Mirrors the shape of the ruleset submitted to the deploy endpoint, so the response can be read back as the desired state.

</summary>

<details>

<summary>

rules: array of <a href="https://developers.cloudflare.com/api/resources/monetization#(resource)%20monetization.rules%20%3E%20(model)%20monetization_rule%20%3E%20(schema)">MonetizationRule</a>

The zone’s payment rules, in the order they are evaluated. Empty when the zone has no payment rules.

</summary>

One of the following:

<details>

<summary>

MonetizationRulesMonetizationRuleInputFixedPrice = <a href="https://developers.cloudflare.com/api/resources/monetization#(resource)%20monetization.rules%20%3E%20(model)%20monetization_rule_input_fixed_price%20%3E%20(schema)">MonetizationRuleInputFixedPrice</a> { address, expression, price, 4 more }

Payment rule with a fixed price set at configuration time.

</summary>

id: string

The server-assigned unique ID of the payment rule. Stable across full-ruleset replacements.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

MonetizationRulesMonetizationRuleInputOriginControlled = <a href="https://developers.cloudflare.com/api/resources/monetization#(resource)%20monetization.rules%20%3E%20(model)%20monetization_rule_input_origin_controlled%20%3E%20(schema)">MonetizationRuleInputOriginControlled</a> { address, expression, scheme, 3 more }

Payment rule whose price the origin server sets dynamically. The rule carries no price and the price field must be omitted — any provided value, including “0”, is rejected because it would not be enforced.

</summary>

id: string

The server-assigned unique ID of the payment rule. Stable across full-ruleset replacements.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List payment rules

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/monetization/rules \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
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
    "rules": [
      {
        "address": "0x1234567890abcdef1234567890abcdef12345678===",
        "expression": "(http.request.uri.path eq \"/premium\" and http.request.method in {\"GET\" \"POST\"})",
        "price": "250000",
        "scheme": "exact",
        "id": "023e105f4ecef8ad9ca31a8372d0c353",
        "description": "Premium API endpoint",
        "enabled": true
      }
    ]
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
    "rules": [
      {
        "address": "0x1234567890abcdef1234567890abcdef12345678===",
        "expression": "(http.request.uri.path eq \"/premium\" and http.request.method in {\"GET\" \"POST\"})",
        "price": "250000",
        "scheme": "exact",
        "id": "023e105f4ecef8ad9ca31a8372d0c353",
        "description": "Premium API endpoint",
        "enabled": true
      }
    ]
  },
  "success": true
}
```