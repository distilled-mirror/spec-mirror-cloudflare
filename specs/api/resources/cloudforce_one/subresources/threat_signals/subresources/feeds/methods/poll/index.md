---
title: Trigger Threat Signals feed poll
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Feeds](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Trigger Threat Signals feed poll

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/poll

Starts an immediate poll of one or all Threat Signals feeds.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20poll%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

feed\_id: optional stringor "all"

</summary>

One of the following:

string

<a href="#">Link to this property</a>

"all"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20poll%20%3E%20(params)%20default%20%3E%20(param)%20feed_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20poll%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {errors, feeds, triggered }

</summary>

errors: number

<a href="#">Link to this property</a>

<details>

<summary>

feeds: array of object {feed\_id, status, workflow\_id, feed\_enabled }

</summary>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

status: "workflow\_created"or "error"

</summary>

One of the following:

"workflow\_created"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

workflow\_id: string

<a href="#">Link to this property</a>

feed\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

triggered: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20poll%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20poll%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Trigger Threat Signals feed poll

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/feeds/poll \
    -X POST \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "result": {
    "errors": 0,
    "feeds": [
      {
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "status": "workflow_created",
        "workflow_id": "workflow_id",
        "feed_enabled": true
      }
    ],
    "triggered": 0
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
      "message": "message"
    }
  ],
  "result": {
    "errors": 0,
    "feeds": [
      {
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "status": "workflow_created",
        "workflow_id": "workflow_id",
        "feed_enabled": true
      }
    ],
    "triggered": 0
  },
  "success": true
}
```