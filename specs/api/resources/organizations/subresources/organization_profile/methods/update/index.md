---
title: Modify organization profile.
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Organizations](https://developers.cloudflare.com/api/resources/organizations)

[Organization Profile](https://developers.cloudflare.com/api/resources/organizations/subresources/organization_profile)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Modify organization profile.

PUT/organizations/{organization\_id}/profile

Partially updates the business profile (name, email, phone, address, and external metadata) associated with this organization’s customer record, creating the profile if it does not exist. Changes apply to every account and organization sharing that profile. Omitted, empty, or null fields are left unchanged. Each profile field is limited to 1,000 UTF-8 bytes. Only available to members of the organization.

##### Security

API Email + API Key

The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**`X-Auth-Email: user@example.com`

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**`X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194`

##### P ath ParametersExpand Collapse

organization\_id: string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20organization_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

business\_address: optional string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20business_address%20%3E%20(schema)>)

business\_email: optional string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20business_email%20%3E%20(schema)>)

business\_name: optional string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20business_name%20%3E%20(schema)>)

business\_phone: optional string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20business_phone%20%3E%20(schema)>)

external\_metadata: optional string

[Link to this property](#)%20organizations.organization_profile%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20external_metadata%20%3E%20(schema)>)

### Modify organization profile.

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/organizations/$ORGANIZATION_ID/profile \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY" \
    -d '{}'
```

##### Returns Examples