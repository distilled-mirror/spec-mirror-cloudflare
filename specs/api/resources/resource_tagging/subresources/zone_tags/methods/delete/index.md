---
title: Delete tags from a zone-level resource
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Resource Tagging](https://developers.cloudflare.com/api/resources/resource_tagging)

[Zone Tags](https://developers.cloudflare.com/api/resources/resource_tagging/subresources/zone_tags)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete tags from a zone-level resource

DELETE/zones/{zone\_id}/tags

Removes all tags from a specific zone-level resource.

##### Security

API Email + API Key

The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**`X-Auth-Email: user@example.com`

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**`X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194`

##### P ath ParametersExpand Collapse

zone\_id: string

Zone ID is required only for zone-level resources

maxLength32

minLength32

[Link to this property](#)%20resource_tagging.zone_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

resource\_id: string

The ID of the resource to remove tags from.

[Link to this property](#)%20resource_tagging.zone_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20resource_id%20%3E%20(schema)>)

<details>

<summary>

resource\_type: "access\_application\_policy"or "api\_gateway\_operation"or "custom\_certificate"or 8 more

The type of the resource.

</summary>

One of the following:

"access\_application\_policy"

<a href="#">Link to this property</a>

"api\_gateway\_operation"

<a href="#">Link to this property</a>

"custom\_certificate"

<a href="#">Link to this property</a>

"custom\_hostname"

<a href="#">Link to this property</a>

"dns\_record"

<a href="#">Link to this property</a>

"healthcheck"

<a href="#">Link to this property</a>

"load\_balancer"

<a href="#">Link to this property</a>

"managed\_client\_certificate"

<a href="#">Link to this property</a>

"worker\_route"

<a href="#">Link to this property</a>

"zone"

<a href="#">Link to this property</a>

"zone\_ruleset"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20resource_tagging.zone_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20resource_type%20%3E%20(schema)>)

access\_application\_id: optional string

Access application ID identifier. Required for access\_application\_policy resources.

formatuuid

[Link to this property](#)%20resource_tagging.zone_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20access_application_id%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

"If-Match": optional string

[Link to this property](#)%20resource_tagging.zone_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20If-Match%20%3E%20(schema)>)

### Delete tags from a zone-level resource

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/tags \
    -X DELETE \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
```

##### Returns Examples