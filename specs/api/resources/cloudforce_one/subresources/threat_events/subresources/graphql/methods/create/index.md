---
title: Run a GraphQL aggregation over events
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Events](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events)

[Graphql](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/graphql)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Run a GraphQL aggregation over events

POST/accounts/{account\_id}/cloudforce-one/events/graphql

Runs a GraphQL aggregation query over events. Supports grouping by multiple fields, date range filters, and aggregation across datasets.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

Account ID.

[Link to this property](#)%20cloudforce_one.threat_events.graphql%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

data: optional unknown

[Link to this property](#)%20cloudforce_one.threat_events.graphql%20%3E%20(model)%20graphql_create_response%20%3E%20(schema)%20%3E%20(property)%20data>)

errors: optional array of unknown

[Link to this property](#)%20cloudforce_one.threat_events.graphql%20%3E%20(model)%20graphql_create_response%20%3E%20(schema)%20%3E%20(property)%20errors>)

### Run a GraphQL aggregation over events

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/events/graphql \
    -X POST \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "data": {},
  "errors": [
    {}
  ]
}
```

##### Returns Examples

200 example

```
{
  "data": {},
  "errors": [
    {}
  ]
}
```