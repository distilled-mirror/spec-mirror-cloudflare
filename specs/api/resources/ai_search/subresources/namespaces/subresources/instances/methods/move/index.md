---
title: Move an instance to a different namespace.
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Search](https://developers.cloudflare.com/api/resources/ai_search)

[Namespaces](https://developers.cloudflare.com/api/resources/ai_search/subresources/namespaces)

[Instances](https://developers.cloudflare.com/api/resources/ai_search/subresources/namespaces/subresources/instances)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Move an instance to a different namespace.

PATCH/accounts/{account\_id}/ai-search/namespaces/{namespace}/instances/{id}

Moves an instance from its current namespace to the specified target namespace. Use ‘default’ with —destination-namespace to move the instance back to the default namespace. Fails with 400 if the target namespace already has an instance with the same id (ids must be unique within a namespace — the same id can exist in different namespaces).

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

account\_id: string

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

namespace: string

Current namespace of the instance.

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(params)%20default%20%3E%20(param)%20namespace%20%3E%20(schema)>)

id: string

Instance id.

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(params)%20default%20%3E%20(param)%20id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

new\_namespace: string

Target namespace to move the instance into.

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(params)%200%20%3E%20(param)%20new_namespace%20%3E%20(schema)>)

##### ReturnsExpand Collapse

result: unknown

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20ai_search.namespaces.instances%20%3E%20(method)%20move%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Move an instance to a different namespace.

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/ai-search/namespaces/$NAMESPACE/instances/$ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "new_namespace": "staging"
        }'
```

200 example

```
{
  "result": {},
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "result": {},
  "success": true
}
```