---
title: Dynamic Script - execute code and return browser session details.
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

[Script](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/script)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Dynamic Script - execute code and return browser session details.

POST/accounts/{account\_id}/browser-rendering/script

Acquires a browser session and runs the provided code in it. The session stays open for reuse; close it with `DELETE /devtools/browser/:sessionId` or `browser.close()`, otherwise it ends at the idle timeout.

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

`Browser Rendering Write`

##### P ath ParametersExpand Collapse

account\_id: string

Account ID.

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

browser: optional "kitesurf"

Rendering backend for this script. Set to `kitesurf` to run it on Kitesurf (beta), which supports CDP only and rejects `keep_alive`, `lab` and `recording`.

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20browser%20%3E%20(schema)>)

keep\_alive: optional number

Keep-alive time in milliseconds

maximum1200000

minimum10000

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20keep_alive%20%3E%20(schema)>)

lab: optional boolean

Use experimental browser.

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20lab%20%3E%20(schema)>)

recording: optional boolean

Record the browser session. Retrieve it with `GET /recording/:session_id`.

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20recording%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

code: string

Function body executed against the selected library’s runner.

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20code%20%3E%20(schema)>)

<details>

<summary>

library: optional "playwright"or "puppeteer"

Library the script runs with. Defaults to raw CDP when omitted.

</summary>

One of the following:

"playwright"

<a href="#">Link to this property</a>

"puppeteer"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20library%20%3E%20(schema)>)

timeout: optional number

Maximum script run time in milliseconds.

maximum120000

minimum1

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20timeout%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

result: stringor numberor booleanor 2 more

The script’s return value, or null when it returned nothing. Arrays nested inside arrays are also returned, but this schema does not describe them.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

array of stringor numberor booleanor map\[unknown]

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20browser_rendering.script%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Dynamic Script - execute code and return browser session details.

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/browser-rendering/script \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "code": "code"
        }'
```

200 example

429 example

```
{
  "result": "string",
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "Rate limit exceeded"
    }
  ],
  "success": false
}
```

##### Returns Examples

200 example

429 example

```
{
  "result": "string",
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "Rate limit exceeded"
    }
  ],
  "success": false
}
```