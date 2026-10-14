---
title: Get Zone Precursor Config
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Precursor](https://developers.cloudflare.com/api/resources/precursor)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get Zone Precursor Config

GET/zones/{zone\_id}/precursor

Retrieve a zone’s Precursor configuration: the detection `mode`, whether to `show_interstitial`, and the ordered list of `rules`.

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

Identifier.

maxLength32

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

"Cloudflare-Version": "1.0"

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20Cloudflare-Version%20%3E%20(schema)>)

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

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional <a href="https://developers.cloudflare.com/api/resources/precursor#(resource)%20precursor%20%3E%20(model)%20precursor_config%20%3E%20(schema)">PrecursorConfig</a> { mode, rules, show\_interstitial }

</summary>

<details>

<summary>

mode: optional "off"or "monitor"or "arm"

Controls Precursor detection for the zone. <code>off</code> disables detection, <code>monitor</code> records detections without affecting bot scores, and <code>arm</code> allows detections to affect bot scores.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"monitor"

<a href="#">Link to this property</a>

"arm"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rules: optional array of object {expression, show\_interstitial, id, 2 more }

The ordered list of Precursor rules for the zone.

</summary>

expression: string

The filter expression that determines which requests the rule matches.

maxLength4000

<a href="#">Link to this property</a>

show\_interstitial: boolean

Whether Precursor shows an interstitial when it takes action on a request.

<a href="#">Link to this property</a>

id: optional string

The read-only identifier that Cloudflare assigns to the rule.

<a href="#">Link to this property</a>

description: optional string

An informative description of the rule.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the rule is active.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_interstitial: optional boolean

Whether Precursor shows an interstitial when it takes action on a request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20precursor%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Get Zone Precursor Config

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/precursor \
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
    "mode": "arm",
    "rules": [
      {
        "expression": "http.request.uri.path eq \"/shop\"",
        "show_interstitial": true,
        "id": "3a03d665bac043e3a684e0d385a4b1e2",
        "description": "Show an interstitial on the shop page",
        "enabled": true
      }
    ],
    "show_interstitial": false
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
    "mode": "arm",
    "rules": [
      {
        "expression": "http.request.uri.path eq \"/shop\"",
        "show_interstitial": true,
        "id": "3a03d665bac043e3a684e0d385a4b1e2",
        "description": "Show an interstitial on the shop page",
        "enabled": true
      }
    ],
    "show_interstitial": false
  }
}
```