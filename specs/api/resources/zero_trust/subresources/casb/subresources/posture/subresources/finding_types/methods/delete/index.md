---
title: Delete a custom finding type
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

[Finding Types](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/finding_types)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete a custom finding type

DELETE/accounts/{account\_id}/data-security/posture/finding\_types/{finding\_type\_id}

Delete an existing custom finding type.

**Security**: Only custom finding types (not system-managed) can be deleted.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

finding\_type\_id: string

formatuuid

[Link to this property](#)%20zero_trust.casb.posture.finding_types%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20finding_type_id%20%3E%20(schema)>)

### Delete a custom finding type

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/data-security/posture/finding_types/$FINDING_TYPE_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

##### Returns Examples