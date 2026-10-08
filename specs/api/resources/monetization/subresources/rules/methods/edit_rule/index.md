---
title: Update a payment rule
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Monetization](https://developers.cloudflare.com/api/resources/monetization)

[Rules](https://developers.cloudflare.com/api/resources/monetization/subresources/rules)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update a payment rule

PATCH/zones/{zone\_id}/monetization/rules/{rule\_id}

Applies a partial update to a single Payment Required rule. Only the fields present in the request body are changed; omitted fields keep their current values. Returns the full resulting rule collection.

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

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

rule\_id: string

maxLength32

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%20default%20%3E%20(param)%20rule_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

address: optional string

0x-prefixed 20-byte hexadecimal Ethereum address. Mixed-case addresses must carry a valid EIP-55 checksum; all-lowercase or all-uppercase addresses are also accepted. The effective address must pass wallet screening whenever the rule is patched.

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20address%20%3E%20(schema)>)

description: optional string

maxLength512

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20description%20%3E%20(schema)>)

enabled: optional boolean

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20enabled%20%3E%20(schema)>)

expression: optional string

Wirefilter expression identifying the requests that require payment. Forwarded verbatim to the Rulesets API, which validates its syntax.

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20expression%20%3E%20(schema)>)

price: optional string

Price in the smallest indivisible unit of the configured payment token, encoded as a decimal string. Must be a canonical decimal integer in \[1000, 100000000]: no leading zeros, and a bare JSON number is rejected. The price is required for the fixed-price schemes (“exact” and “upto”) and must be at least 1000, the smallest amount the payment facilitator can settle ($0.001 for a 6-decimal token such as USDC), and at most 100000000 ($100 for a 6-decimal token). When the scheme is “origin\_controlled” the origin server sets pricing dynamically and the rule carries no price: the field must be omitted — any provided value, including “0”, is rejected because it would not be enforced. Responses always encode this as a string and omit it for “origin\_controlled” rules; the pattern matches exactly the set of values the server accepts.

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20price%20%3E%20(schema)>)

<details>

<summary>

scheme: optional "exact"or "upto"or "origin\_controlled"

X402 payment scheme. “exact” requires the specified payment amount; “upto” permits a payment up to the specified amount; “origin\_controlled” lets the origin server set pricing dynamically, in which case the rule carries no price and the price field must be omitted.

</summary>

One of the following:

"exact"

<a href="#">Link to this property</a>

"upto"

<a href="#">Link to this property</a>

"origin\_controlled"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(params)%200%20%3E%20(param)%20scheme%20%3E%20(schema)>)

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

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message }

</summary>

code: optional number

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

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

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20monetization.rules%20%3E%20(method)%20edit_rule%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Update a payment rule

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/monetization/rules/$RULE_ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "address": "0x1234567890abcdef1234567890abcdef12345678===",
          "description": "Premium API endpoint",
          "expression": "(http.request.uri.path eq \\"/premium\\" and http.request.method in {\\"GET\\" \\"POST\\"})",
          "price": "250000",
          "scheme": "exact"
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