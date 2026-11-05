---
title: Get bot details
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Radar](https://developers.cloudflare.com/api/resources/radar)

[Bots](https://developers.cloudflare.com/api/resources/radar/subresources/bots)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get bot details

GET/radar/bots/{bot\_slug}

Retrieves the requested bot information.

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

`User Details Write``User Details Read`

##### P ath ParametersExpand Collapse

bot\_slug: string

Bot slug.

maxLength100

[Link to this property](#)%20radar.bots%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20bot_slug%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

format: optional "JSON"or "CSV"

Format in which results will be returned.

</summary>

One of the following:

"JSON"

<a href="#">Link to this property</a>

"CSV"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20radar.bots%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20format%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

result: object {bot }

</summary>

<details>

<summary>

bot: object {accessLevel, categories, category, 12 more }

</summary>

accessLevel: string

Who can operate the bot: DIRECT bots reach origins under their own identity, while INTERMEDIARY bots forward requests on behalf of another agent or a person.

<a href="#">Link to this property</a>

categories: array of string

The categories of the bot.

<a href="#">Link to this property</a>

Deprecatedcategory: string

The category of the bot. Deprecated: use <code>categories</code>.

<a href="#">Link to this property</a>

contentUse: string

How the bot uses the content it fetches (e.g., immediate, reference or full).

<a href="#">Link to this property</a>

description: string

A summary for the bot (e.g., purpose).

<a href="#">Link to this property</a>

documentationUrl: string

The link to the bot documentation.

<a href="#">Link to this property</a>

Deprecatedkind: string

The kind of the bot.

<a href="#">Link to this property</a>

name: string

The name of the bot.

<a href="#">Link to this property</a>

operator: string

The organization that owns and operates the bot.

<a href="#">Link to this property</a>

DeprecatedoperatorUrl: string

The link to the bot documentation. Deprecated: use <code>documentationUrl</code>.

<a href="#">Link to this property</a>

operatorWebsiteUrl: string

The link to the operator’s website.

<a href="#">Link to this property</a>

slug: string

A kebab-case identifier derived from the bot name.

<a href="#">Link to this property</a>

userAgentPatterns: array of string

<a href="#">Link to this property</a>

userAgents: array of string

<a href="#">Link to this property</a>

signatureAgentUrl: optional string

The URL of the agent’s <a href="https://blog.cloudflare.com/web-bot-auth/">Web Bot Auth</a> resource. Null for bots not verified via request signature.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20radar.bots%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20radar.bots%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get bot details

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/radar/bots/$BOT_SLUG \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "result": {
    "bot": {
      "accessLevel": "DIRECT",
      "categories": [
        "AI_CRAWLER"
      ],
      "category": "AI_CRAWLER",
      "contentUse": "full",
      "description": "OpenAI/ChatGPT's web crawler",
      "documentationUrl": "https://platform.openai.com/docs/bots",
      "kind": "AGENT",
      "name": "GPTBot",
      "operator": "OpenAI",
      "operatorUrl": "https://platform.openai.com/docs/bots",
      "operatorWebsiteUrl": "https://openai.com",
      "slug": "gptbot",
      "userAgentPatterns": [
        "GPTBot"
      ],
      "userAgents": [
        "GPTBot"
      ],
      "signatureAgentUrl": "https://example.com/signature-agent"
    }
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "result": {
    "bot": {
      "accessLevel": "DIRECT",
      "categories": [
        "AI_CRAWLER"
      ],
      "category": "AI_CRAWLER",
      "contentUse": "full",
      "description": "OpenAI/ChatGPT's web crawler",
      "documentationUrl": "https://platform.openai.com/docs/bots",
      "kind": "AGENT",
      "name": "GPTBot",
      "operator": "OpenAI",
      "operatorUrl": "https://platform.openai.com/docs/bots",
      "operatorWebsiteUrl": "https://openai.com",
      "slug": "gptbot",
      "userAgentPatterns": [
        "GPTBot"
      ],
      "userAgents": [
        "GPTBot"
      ],
      "signatureAgentUrl": "https://example.com/signature-agent"
    }
  },
  "success": true
}
```