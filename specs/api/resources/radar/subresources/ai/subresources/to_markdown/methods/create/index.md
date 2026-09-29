---
title: Convert uploaded files to Markdown
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Radar](https://developers.cloudflare.com/api/resources/radar)

[AI](https://developers.cloudflare.com/api/resources/radar/subresources/ai)

[To Markdown](https://developers.cloudflare.com/api/resources/radar/subresources/ai/subresources/to_markdown)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Convert uploaded files to Markdown

Deprecated: Use \[AI > To Markdown](https://developers.cloudflare.com/api/resources/ai/subresources/to\_markdown/) instead.

POST/accounts/{account\_id}/ai/tomarkdown

Converts files uploaded as multipart form data into Markdown using Workers AI. Returns a conversion result for each file. Use the supported-formats endpoint to check accepted file types.

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

`Workers AI Write``Workers AI Read`

##### P ath ParametersExpand Collapse

account\_id: string

Cloudflare account ID used for this AI model request.

[Link to this property](#)%20radar.ai.to_markdown%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersForm DataExpand Collapse

files: array of string

Files to convert, supplied as multipart file uploads.

[Link to this property](#)%20radar.ai.to_markdown%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20files%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

result: array of object {data, format, mimeType, 2 more }

</summary>

data: string

<a href="#">Link to this property</a>

format: string

<a href="#">Link to this property</a>

mimeType: string

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

tokens: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20radar.ai.to_markdown%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20radar.ai.to_markdown%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Convert uploaded files to Markdown

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai/tomarkdown \
    -H 'Content-Type: multipart/form-data' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -F files='["Example data"]'
```

200 example

```
{
  "result": [
    {
      "data": "data",
      "format": "format",
      "mimeType": "mimeType",
      "name": "name",
      "tokens": "tokens"
    }
  ],
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "result": [
    {
      "data": "data",
      "format": "format",
      "mimeType": "mimeType",
      "name": "name",
      "tokens": "tokens"
    }
  ],
  "success": true
}
```