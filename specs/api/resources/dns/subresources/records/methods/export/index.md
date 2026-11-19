---
title: Export DNS Records
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[DNS](https://developers.cloudflare.com/api/resources/dns)

[Records](https://developers.cloudflare.com/api/resources/dns/subresources/records)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Export DNS Records

GET/zones/{zone\_id}/dns\_records/export

Export your [BIND config](https://en.wikipedia.org/wiki/Zone_file "Zone file") through this endpoint. Use the same record filters as the List DNS Records endpoint to export only matching stored records.

By default, the SOA record (stored or generated) and assigned apex NS records, where applicable, are included regardless of filters. Secondary zones must have a stored SOA record to export in this mode. Set `include_generated_records=false` to export only matching stored records, without adding the SOA/nameserver section or requiring secondary zones to have an SOA record. Matching stored SOA and NS records are still exported. This may produce a partial zone rather than a complete zone. Workers-managed records are never exported.

The export returns at most 5,000,000 matching stored records, in addition to any automatically included SOA and assigned apex NS records. It is not paginated and does not support `page`, `per_page`, `order`, `direction`, `cursor`, or `prev_cursor`.

`include_shadow_metadata=true` is required when using `shadowed_by_name`; it does not add shadow metadata to the BIND output.

See [the documentation](https://developers.cloudflare.com/dns/manage-dns-records/how-to/import-and-export/ "Import and export records") for more information.

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

`DNS Read``DNS Write`

##### P ath ParametersExpand Collapse

zone\_id: string

Identifier.

maxLength32

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

comment: optional object {absent, contains, endswith, 3 more }

</summary>

absent: optional string

If this parameter is present, only records *without* a comment are returned.

<a href="#">Link to this property</a>

contains: optional string

Substring of the DNS record comment. Comment filters are case-insensitive.

<a href="#">Link to this property</a>

endswith: optional string

Suffix of the DNS record comment. Comment filters are case-insensitive.

<a href="#">Link to this property</a>

exact: optional string

Exact value of the DNS record comment. Comment filters are case-insensitive.

<a href="#">Link to this property</a>

present: optional string

If this parameter is present, only records *with* a comment are returned.

<a href="#">Link to this property</a>

startswith: optional string

Prefix of the DNS record comment. Comment filters are case-insensitive.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20comment%20%3E%20(schema)>)

<details>

<summary>

content: optional object {contains, endswith, exact, startswith }

</summary>

contains: optional string

Substring of the DNS record content. Content filters are case-insensitive.

<a href="#">Link to this property</a>

endswith: optional string

Suffix of the DNS record content. Content filters are case-insensitive.

<a href="#">Link to this property</a>

exact: optional string

Exact value of the DNS record content. Content filters are case-insensitive.

<a href="#">Link to this property</a>

startswith: optional string

Prefix of the DNS record content. Content filters are case-insensitive.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20content%20%3E%20(schema)>)

include\_generated\_records: optional boolean

Whether to add the SOA and assigned apex NS records independently of the record filters. Set to `false` to export only matching stored records. Matching stored SOA and NS records are still exported.

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20include_generated_records%20%3E%20(schema)>)

include\_shadow\_metadata: optional boolean

Set to `true` to enable the `shadowed_by_name` filter. This does not add shadow metadata to the BIND output.

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20include_shadow_metadata%20%3E%20(schema)>)

<details>

<summary>

match: optional "any"or "all"

Whether to match all search requirements or at least one (any). If set to <code>all</code>, acts like a logical AND between filters. If set to <code>any</code>, acts like a logical OR instead. Note that the interaction between tag filters is controlled by the <code>tag-match</code> parameter instead.

</summary>

One of the following:

"any"

<a href="#">Link to this property</a>

"all"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20match%20%3E%20(schema)>)

<details>

<summary>

name: optional object {contains, endswith, exact, startswith }

</summary>

contains: optional string

Substring of the DNS record name. Name filters are case-insensitive.

<a href="#">Link to this property</a>

endswith: optional string

Suffix of the DNS record name. Name filters are case-insensitive.

<a href="#">Link to this property</a>

exact: optional string

Exact value of the DNS record name. Name filters are case-insensitive.

<a href="#">Link to this property</a>

startswith: optional string

Prefix of the DNS record name. Name filters are case-insensitive.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20name%20%3E%20(schema)>)

proxied: optional boolean

Whether the record is receiving the performance and security benefits of Cloudflare.

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20proxied%20%3E%20(schema)>)

search: optional string

Allows searching in multiple properties of a DNS record simultaneously. This parameter is intended for human users, not automation. Its exact behavior is intentionally left unspecified and is subject to change in the future. This parameter works independently of the `match` setting. For automated searches, please use the other available parameters.

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20search%20%3E%20(schema)>)

shadowed\_by\_name: optional string

Filters the response to records at or below the specified NS delegation name. NS, DS, and NSEC records at the delegation name are excluded because they are not shadowed by that delegation. Those record types are included only when they exist below the delegation. The value must be a non-apex subdomain of the zone. Requires `include_shadow_metadata=true`. See [Shadowed records](https://developers.cloudflare.com/dns/manage-dns-records/reference/shadowed-records).

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20shadowed_by_name%20%3E%20(schema)>)

shadowing\_name: optional string

Returns NS records that shadow the given name, searching at the name itself and each of its ancestor names within the zone, excluding the zone apex. The value must be a subdomain of the zone; the zone apex is not accepted. See [Shadowed records](https://developers.cloudflare.com/dns/manage-dns-records/reference/shadowed-records).

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20shadowing_name%20%3E%20(schema)>)

<details>

<summary>

tag: optional object {absent, contains, endswith, 3 more }

</summary>

absent: optional string

Name of a tag which must *not* be present on the DNS record. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

contains: optional string

A tag and value, of the form <code>&lt;tag-name&gt;:&lt;tag-value&gt;</code>. The API will only return DNS records that have a tag named <code>&lt;tag-name&gt;</code> whose value contains <code>&lt;tag-value&gt;</code>. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

endswith: optional string

A tag and value, of the form <code>&lt;tag-name&gt;:&lt;tag-value&gt;</code>. The API will only return DNS records that have a tag named <code>&lt;tag-name&gt;</code> whose value ends with <code>&lt;tag-value&gt;</code>. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

exact: optional string

A tag and value, of the form <code>&lt;tag-name&gt;:&lt;tag-value&gt;</code>. The API will only return DNS records that have a tag named <code>&lt;tag-name&gt;</code> whose value is <code>&lt;tag-value&gt;</code>. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

present: optional string

Name of a tag which must be present on the DNS record. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

startswith: optional string

A tag and value, of the form <code>&lt;tag-name&gt;:&lt;tag-value&gt;</code>. The API will only return DNS records that have a tag named <code>&lt;tag-name&gt;</code> whose value starts with <code>&lt;tag-value&gt;</code>. Tag filters are case-insensitive.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20tag%20%3E%20(schema)>)

<details>

<summary>

tag\_match: optional "any"or "all"

Whether to match all tag search requirements or at least one (any). If set to <code>all</code>, acts like a logical AND between tag filters. If set to <code>any</code>, acts like a logical OR instead. Note that the regular <code>match</code> parameter is still used to combine the resulting condition with other filters that aren’t related to tags. The legacy <code>tag-match</code> parameter is an alias for this parameter.

</summary>

One of the following:

"any"

<a href="#">Link to this property</a>

"all"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20tag_match%20%3E%20(schema)>)

<details>

<summary>

type: optional "A"or "AAAA"or "CAA"or 18 more

Record type.

</summary>

One of the following:

"A"

<a href="#">Link to this property</a>

"AAAA"

<a href="#">Link to this property</a>

"CAA"

<a href="#">Link to this property</a>

"CERT"

<a href="#">Link to this property</a>

"CNAME"

<a href="#">Link to this property</a>

"DNSKEY"

<a href="#">Link to this property</a>

"DS"

<a href="#">Link to this property</a>

"HTTPS"

<a href="#">Link to this property</a>

"LOC"

<a href="#">Link to this property</a>

"MX"

<a href="#">Link to this property</a>

"NAPTR"

<a href="#">Link to this property</a>

"NS"

<a href="#">Link to this property</a>

"OPENPGPKEY"

<a href="#">Link to this property</a>

"PTR"

<a href="#">Link to this property</a>

"SMIMEA"

<a href="#">Link to this property</a>

"SRV"

<a href="#">Link to this property</a>

"SSHFP"

<a href="#">Link to this property</a>

"SVCB"

<a href="#">Link to this property</a>

"TLSA"

<a href="#">Link to this property</a>

"TXT"

<a href="#">Link to this property</a>

"URI"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.records%20%3E%20(method)%20export%20%3E%20(params)%20default%20%3E%20(param)%20type%20%3E%20(schema)>)

### Export DNS Records

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/dns_records/export \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

##### Returns Examples