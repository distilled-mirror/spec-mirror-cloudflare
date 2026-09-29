---
title: Replace Threat Signals skill tag categories
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Skills](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills)

[Tag Categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills/subresources/tag_categories)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Replace Threat Signals skill tag categories

PUT/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills/{skill\_id}/tag-categories

Replaces the tag categories the default tagging skill may choose tags from.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

skill\_id: "default-tagging-skill"

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20skill_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

category\_uuids: array of string

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20category_uuids%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {category\_uuids, skill\_id }

</summary>

category\_uuids: array of string

<a href="#">Link to this property</a>

skill\_id: "default-tagging-skill"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.skills.tag_categories%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Replace Threat Signals skill tag categories

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/skills/$SKILL_ID/tag-categories \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "category_uuids": [
            "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
          ]
        }'
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
    "category_uuids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "skill_id": "default-tagging-skill"
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
    "category_uuids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "skill_id": "default-tagging-skill"
  },
  "success": true
}
```