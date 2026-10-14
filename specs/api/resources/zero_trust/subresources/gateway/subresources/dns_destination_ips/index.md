---
title: DNS Destination IPs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Gateway](https://developers.cloudflare.com/api/resources/zero_trust/subresources/gateway)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# DNS Destination IPs

##### [List Zero Trust Gateway DNS destination IPv4 address pairs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/gateway/subresources/dns_destination_ips/methods/list)

GET/accounts/{account\_id}/gateway/dns\_destination\_ips

##### ModelsExpand Collapse

DNSDestinationIPs = string

Indicate the identifier of the pair of IPv4 addresses assigned to this location.

[Link to this property](#)%20zero_trust.gateway.dns_destination_ips%20%3E%20(model)%20dns_destination_ips%20%3E%20(schema)>)

<details>

<summary>

DNSDestinationIPListResponse object {id, backup\_ip, pair\_type, primary\_ip }

</summary>

id: string

<a href="#">Link to this property</a>

backup\_ip: string

<a href="#">Link to this property</a>

<details>

<summary>

pair\_type: "shared"or "dedicated"or "byoip"

Specify whether the pair shared across multiple accounts (shared) or available exclusively to this account. Non-shared pairs can contain Cloudflare-owned IPs (dedicated) or customer-provided IPs (byoip).

</summary>

One of the following:

"shared"

<a href="#">Link to this property</a>

"dedicated"

<a href="#">Link to this property</a>

"byoip"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

primary\_ip: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.gateway.dns_destination_ips%20%3E%20(model)%20dns_destination_ip_list_response%20%3E%20(schema)>)