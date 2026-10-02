---
title: Nameserver Sets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[DNS](https://developers.cloudflare.com/api/resources/dns)

[Settings](https://developers.cloudflare.com/api/resources/dns/subresources/settings)

[Account](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Nameserver Sets

##### [List Custom Nameserver Sets](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account/subresources/nameserver_sets/methods/list)

GET/accounts/{account\_id}/dns\_settings/nameserver\_sets

##### [Get Custom Nameserver Set](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account/subresources/nameserver_sets/methods/get)

GET/accounts/{account\_id}/dns\_settings/nameserver\_sets/{nameserver\_set\_id}

##### [Create Custom Nameserver Set](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account/subresources/nameserver_sets/methods/create)

POST/accounts/{account\_id}/dns\_settings/nameserver\_sets

##### [Delete Custom Nameserver Set](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account/subresources/nameserver_sets/methods/delete)

DELETE/accounts/{account\_id}/dns\_settings/nameserver\_sets/{nameserver\_set\_id}

##### ModelsExpand Collapse

<details>

<summary>

NameserverSetListResponse = object {id, advanced, created\_on, 2 more } or object {id, advanced, created\_on, 2 more }

</summary>

One of the following:

<details>

<summary>

DNSSettingsNameserverSetStandardResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: false

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv6, name }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DNSSettingsNameserverSetAdvancedResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: true

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv4\_groups, ipv6, 2 more }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv4\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv6\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(model)%20nameserver_set_list_response%20%3E%20(schema)>)

<details>

<summary>

NameserverSetGetResponse = object {id, advanced, created\_on, 2 more } or object {id, advanced, created\_on, 2 more }

</summary>

One of the following:

<details>

<summary>

DNSSettingsNameserverSetStandardResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: false

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv6, name }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DNSSettingsNameserverSetAdvancedResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: true

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv4\_groups, ipv6, 2 more }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv4\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv6\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(model)%20nameserver_set_get_response%20%3E%20(schema)>)

<details>

<summary>

NameserverSetCreateResponse = object {id, advanced, created\_on, 2 more } or object {id, advanced, created\_on, 2 more }

</summary>

One of the following:

<details>

<summary>

DNSSettingsNameserverSetStandardResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: false

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv6, name }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DNSSettingsNameserverSetAdvancedResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: true

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv4\_groups, ipv6, 2 more }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv4\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv6\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(model)%20nameserver_set_create_response%20%3E%20(schema)>)

<details>

<summary>

NameserverSetDeleteResponse object {id }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(model)%20nameserver_set_delete_response%20%3E%20(schema)>)