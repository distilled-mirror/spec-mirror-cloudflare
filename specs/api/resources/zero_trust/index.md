---
title: Zero Trust
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Zero Trust

#### Zero TrustDevices

##### [List devices (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/methods/list)

Deprecated

GET/accounts/{account\_id}/devices

##### [Get device (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/methods/get)

Deprecated

GET/accounts/{account\_id}/devices/{device\_id}

##### ModelsExpand Collapse

<details>

<summary>

Device object {id, created, deleted, 17 more }

</summary>

id: optional string

Registration ID. Equal to Device ID except for accounts which enabled <a href="https://developers.cloudflare.com/cloudflare-one/connections/connect-devices/warp/deployment/mdm-deployment/windows-multiuser/">multi-user mode</a>.

maxLength36

<a href="#">Link to this property</a>

created: optional string

When the device was created.

formatdate-time

<a href="#">Link to this property</a>

deleted: optional boolean

True if the device was deleted.

<a href="#">Link to this property</a>

<details>

<summary>

device\_type: optional "windows"or "mac"or "linux"or 3 more

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"android"

<a href="#">Link to this property</a>

"ios"

<a href="#">Link to this property</a>

"chromeos"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

ip: optional string

IPv4 or IPv6 address.

<a href="#">Link to this property</a>

key: optional string

The device’s public key.

<a href="#">Link to this property</a>

last\_seen: optional string

When the device last connected to Cloudflare services.

formatdate-time

<a href="#">Link to this property</a>

mac\_address: optional string

The device mac address.

<a href="#">Link to this property</a>

manufacturer: optional string

The device manufacturer name.

<a href="#">Link to this property</a>

model: optional string

The device model name.

<a href="#">Link to this property</a>

name: optional string

The device name.

<a href="#">Link to this property</a>

os\_distro\_name: optional string

The Linux distro name.

<a href="#">Link to this property</a>

os\_distro\_revision: optional string

The Linux distro revision.

<a href="#">Link to this property</a>

os\_version: optional string

The operating system version.

<a href="#">Link to this property</a>

os\_version\_extra: optional string

Additional operating system version details. For Windows, the UBR (Update Build Revision). For Mac or iOS, the Product Version Extra. For Linux, the distribution name and version.

<a href="#">Link to this property</a>

revoked\_at: optional string

When the device was revoked.

formatdate-time

<a href="#">Link to this property</a>

serial\_number: optional string

The device serial number.

<a href="#">Link to this property</a>

updated: optional string

When the device was updated.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

user: optional object {id, email, name }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: optional string

The WARP client version.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices%20%3E%20(model)%20device%20%3E%20(schema)>)

<details>

<summary>

DeviceGetResponse object {id, account, created, 16 more }

</summary>

id: optional string

Registration ID. Equal to Device ID except for accounts which enabled <a href="https://developers.cloudflare.com/cloudflare-one/connections/connect-devices/warp/deployment/mdm-deployment/windows-multiuser/">multi-user mode</a>.

maxLength36

<a href="#">Link to this property</a>

<details>

<summary>

account: optional object {id, account\_type, name }

</summary>

Deprecatedid: optional string

<a href="#">Link to this property</a>

Deprecatedaccount\_type: optional string

<a href="#">Link to this property</a>

name: optional string

The name of the enrolled account.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created: optional string

When the device was created.

formatdate-time

<a href="#">Link to this property</a>

deleted: optional boolean

True if the device was deleted.

<a href="#">Link to this property</a>

device\_type: optional string

<a href="#">Link to this property</a>

Deprecatedgateway\_device\_id: optional string

<a href="#">Link to this property</a>

ip: optional string

IPv4 or IPv6 address.

<a href="#">Link to this property</a>

key: optional string

The device’s public key.

<a href="#">Link to this property</a>

key\_type: optional string

Type of the key.

<a href="#">Link to this property</a>

last\_seen: optional string

When the device last connected to Cloudflare services.

formatdate-time

<a href="#">Link to this property</a>

mac\_address: optional string

The device mac address.

<a href="#">Link to this property</a>

model: optional string

The device model name.

<a href="#">Link to this property</a>

name: optional string

The device name.

<a href="#">Link to this property</a>

os\_version: optional string

The operating system version.

<a href="#">Link to this property</a>

serial\_number: optional string

The device serial number.

<a href="#">Link to this property</a>

tunnel\_type: optional string

Type of the tunnel connection used.

<a href="#">Link to this property</a>

updated: optional string

When the device was updated.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

user: optional object {id, email, name }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: optional string

The WARP client version.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices%20%3E%20(model)%20device_get_response%20%3E%20(schema)>)

#### Zero TrustDevicesDevices

##### [List devices](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/devices/methods/list)

GET/accounts/{account\_id}/devices/physical-devices

##### [Get device](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/devices/methods/get)

GET/accounts/{account\_id}/devices/physical-devices/{device\_id}

##### [Delete device](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/devices/methods/delete)

DELETE/accounts/{account\_id}/devices/physical-devices/{device\_id}

##### [Revoke device registrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/devices/methods/revoke)

Deprecated

POST/accounts/{account\_id}/devices/physical-devices/{device\_id}/revoke

##### ModelsExpand Collapse

<details>

<summary>

DeviceListResponse object {id, active\_registrations, created\_at, 17 more }

A WARP Device.

</summary>

id: string

The unique ID of the device.

<a href="#">Link to this property</a>

active\_registrations: number

The number of active registrations for the device. Active registrations are those which haven’t been revoked or deleted.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339 timestamp when the device was created.

<a href="#">Link to this property</a>

last\_seen\_at: string

The RFC3339 timestamp when the device was last seen.

<a href="#">Link to this property</a>

name: string

The name of the device.

<a href="#">Link to this property</a>

tags: map\[string]

Tags assigned to the device. An empty object if the device has no tags.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp when the device was last updated.

<a href="#">Link to this property</a>

client\_version: optional string

Version of the WARP client.

<a href="#">Link to this property</a>

deleted\_at: optional string

The RFC3339 timestamp when the device was deleted.

<a href="#">Link to this property</a>

device\_type: optional string

The device operating system.

<a href="#">Link to this property</a>

hardware\_id: optional string

A string that uniquely identifies the hardware or virtual machine (VM).

<a href="#">Link to this property</a>

<details>

<summary>

last\_seen\_registration: optional object {policy }

The last seen registration for the device.

</summary>

<details>

<summary>

policy: optional object {id, default, deleted, 2 more }

A summary of the device profile evaluated for the registration.

</summary>

id: string

The ID of the device settings profile.

<a href="#">Link to this property</a>

default: boolean

Whether the device settings profile is the default profile for the account.

<a href="#">Link to this property</a>

deleted: boolean

Whether the device settings profile was deleted.

<a href="#">Link to this property</a>

name: string

The name of the device settings profile.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp of when the device settings profile last changed for the registration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

last\_seen\_user: optional object {id, email, name }

The last user to use the WARP device.

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mac\_address: optional string

The device MAC address.

<a href="#">Link to this property</a>

manufacturer: optional string

The device manufacturer.

<a href="#">Link to this property</a>

model: optional string

The model name of the device.

<a href="#">Link to this property</a>

os\_version: optional string

The device operating system version number.

<a href="#">Link to this property</a>

os\_version\_extra: optional string

Additional operating system version details. For Windows, the UBR (Update Build Revision). For Mac or iOS, the Product Version Extra. For Linux, the distribution name and version.

<a href="#">Link to this property</a>

Deprecatedpublic\_ip: optional string

**Deprecated**: IP information is provided by DEX - see <a href="https://developers.cloudflare.com/api/resources/zero_trust/subresources/dex/subresources/fleet_status/subresources/devices/methods/list/">https://developers.cloudflare.com/api/resources/zero\_trust/subresources/dex/subresources/fleet\_status/subresources/devices/methods/list/</a>

<a href="#">Link to this property</a>

serial\_number: optional string

The device serial number.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.devices%20%3E%20(model)%20device_list_response%20%3E%20(schema)>)

<details>

<summary>

DeviceGetResponse object {id, active\_registrations, created\_at, 17 more }

A WARP Device.

</summary>

id: string

The unique ID of the device.

<a href="#">Link to this property</a>

active\_registrations: number

The number of active registrations for the device. Active registrations are those which haven’t been revoked or deleted.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339 timestamp when the device was created.

<a href="#">Link to this property</a>

last\_seen\_at: string

The RFC3339 timestamp when the device was last seen.

<a href="#">Link to this property</a>

name: string

The name of the device.

<a href="#">Link to this property</a>

tags: map\[string]

Tags assigned to the device. An empty object if the device has no tags.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp when the device was last updated.

<a href="#">Link to this property</a>

client\_version: optional string

Version of the WARP client.

<a href="#">Link to this property</a>

deleted\_at: optional string

The RFC3339 timestamp when the device was deleted.

<a href="#">Link to this property</a>

device\_type: optional string

The device operating system.

<a href="#">Link to this property</a>

hardware\_id: optional string

A string that uniquely identifies the hardware or virtual machine (VM).

<a href="#">Link to this property</a>

<details>

<summary>

last\_seen\_registration: optional object {policy }

The last seen registration for the device.

</summary>

<details>

<summary>

policy: optional object {id, default, deleted, 2 more }

A summary of the device profile evaluated for the registration.

</summary>

id: string

The ID of the device settings profile.

<a href="#">Link to this property</a>

default: boolean

Whether the device settings profile is the default profile for the account.

<a href="#">Link to this property</a>

deleted: boolean

Whether the device settings profile was deleted.

<a href="#">Link to this property</a>

name: string

The name of the device settings profile.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp of when the device settings profile last changed for the registration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

last\_seen\_user: optional object {id, email, name }

The last user to use the WARP device.

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mac\_address: optional string

The device MAC address.

<a href="#">Link to this property</a>

manufacturer: optional string

The device manufacturer.

<a href="#">Link to this property</a>

model: optional string

The model name of the device.

<a href="#">Link to this property</a>

os\_version: optional string

The device operating system version number.

<a href="#">Link to this property</a>

os\_version\_extra: optional string

Additional operating system version details. For Windows, the UBR (Update Build Revision). For Mac or iOS, the Product Version Extra. For Linux, the distribution name and version.

<a href="#">Link to this property</a>

Deprecatedpublic\_ip: optional string

**Deprecated**: IP information is provided by DEX - see <a href="https://developers.cloudflare.com/api/resources/zero_trust/subresources/dex/subresources/fleet_status/subresources/devices/methods/list/">https://developers.cloudflare.com/api/resources/zero\_trust/subresources/dex/subresources/fleet\_status/subresources/devices/methods/list/</a>

<a href="#">Link to this property</a>

serial\_number: optional string

The device serial number.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.devices%20%3E%20(model)%20device_get_response%20%3E%20(schema)>)

DeviceDeleteResponse = unknown

[Link to this property](#)%20zero_trust.devices.devices%20%3E%20(model)%20device_delete_response%20%3E%20(schema)>)

DeviceRevokeResponse = unknown

[Link to this property](#)%20zero_trust.devices.devices%20%3E%20(model)%20device_revoke_response%20%3E%20(schema)>)

#### Zero TrustDevicesResilience

#### Zero TrustDevicesResilienceGlobal WARP Override

##### [Get Global Disconnect](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/resilience/subresources/global_warp_override/methods/get)

GET/accounts/{account\_id}/devices/resilience/disconnect

##### [Set Global Disconnect](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/resilience/subresources/global_warp_override/methods/create)

POST/accounts/{account\_id}/devices/resilience/disconnect

##### ModelsExpand Collapse

<details>

<summary>

GlobalWARPOverrideGetResponse object {disconnect, timestamp }

</summary>

disconnect: optional boolean

Disconnects all devices on the account using Global WARP override.

<a href="#">Link to this property</a>

timestamp: optional string

When the Global WARP override state was updated.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.resilience.global_warp_override%20%3E%20(model)%20global_warp_override_get_response%20%3E%20(schema)>)

<details>

<summary>

GlobalWARPOverrideCreateResponse object {disconnect, timestamp }

</summary>

disconnect: optional boolean

Disconnects all devices on the account using Global WARP override.

<a href="#">Link to this property</a>

timestamp: optional string

When the Global WARP override state was updated.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.resilience.global_warp_override%20%3E%20(model)%20global_warp_override_create_response%20%3E%20(schema)>)

#### Zero TrustDevicesRegistrations

##### [List registrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/list)

GET/accounts/{account\_id}/devices/registrations

##### [Get registration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/get)

GET/accounts/{account\_id}/devices/registrations/{registration\_id}

##### [Delete registration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/delete)

DELETE/accounts/{account\_id}/devices/registrations/{registration\_id}

##### [Delete registrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/bulk_delete)

DELETE/accounts/{account\_id}/devices/registrations

##### [Revoke registrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/revoke)

Deprecated

POST/accounts/{account\_id}/devices/registrations/revoke

##### [Unrevoke registrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/registrations/methods/unrevoke)

Deprecated

POST/accounts/{account\_id}/devices/registrations/unrevoke

##### ModelsExpand Collapse

<details>

<summary>

RegistrationListResponse object {id, created\_at, device, 12 more }

A WARP configuration tied to a single user. Multiple registrations can be created from a single WARP device.

</summary>

id: string

The ID of the registration.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339 timestamp when the registration was created.

<a href="#">Link to this property</a>

<details>

<summary>

device: object {id, name, client\_version }

Device details embedded inside of a registration.

</summary>

id: string

The ID of the device.

<a href="#">Link to this property</a>

name: string

The name of the device.

<a href="#">Link to this property</a>

client\_version: optional string

Version of the WARP client.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key: string

The public key used to connect to the Cloudflare network.

<a href="#">Link to this property</a>

last\_seen\_at: string

The RFC3339 timestamp when the registration was last seen.

<a href="#">Link to this property</a>

<details>

<summary>

registration\_type: "warp"or "browser\_extension"

The registration client type, derived from device\_type.

</summary>

One of the following:

"warp"

<a href="#">Link to this property</a>

"browser\_extension"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp when the registration was last updated.

<a href="#">Link to this property</a>

deleted\_at: optional string

The RFC3339 timestamp when the registration was deleted.

<a href="#">Link to this property</a>

key\_type: optional string

The type of encryption key used by the WARP client for the active key. Currently ‘curve25519’ for WireGuard and ‘secp256r1’ for MASQUE.

<a href="#">Link to this property</a>

<details>

<summary>

policy: optional object {id, default, deleted, 2 more }

The device settings profile assigned to this registration.

</summary>

id: string

The ID of the device settings profile.

<a href="#">Link to this property</a>

default: boolean

Whether the device settings profile is the default profile for the account.

<a href="#">Link to this property</a>

deleted: boolean

Whether the device settings profile was deleted.

<a href="#">Link to this property</a>

name: string

The name of the device settings profile.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp of when the device settings profile last changed for the registration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

revoked\_at: optional string

The RFC3339 timestamp when the registration was revoked.

<a href="#">Link to this property</a>

tunnel\_type: optional string

Type of the tunnel - wireguard or masque.

<a href="#">Link to this property</a>

<details>

<summary>

user: optional object {id, email, name }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

virtual\_ipv4: optional string

The virtual IPv4 address assigned to the network interface of the tunnel for this registration.

<a href="#">Link to this property</a>

virtual\_ipv6: optional string

The virtual IPv6 address assigned to the network interface of the tunnel for this registration.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_list_response%20%3E%20(schema)>)

<details>

<summary>

RegistrationGetResponse object {id, created\_at, device, 12 more }

A WARP configuration tied to a single user. Multiple registrations can be created from a single WARP device.

</summary>

id: string

The ID of the registration.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339 timestamp when the registration was created.

<a href="#">Link to this property</a>

<details>

<summary>

device: object {id, name, client\_version }

Device details embedded inside of a registration.

</summary>

id: string

The ID of the device.

<a href="#">Link to this property</a>

name: string

The name of the device.

<a href="#">Link to this property</a>

client\_version: optional string

Version of the WARP client.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key: string

The public key used to connect to the Cloudflare network.

<a href="#">Link to this property</a>

last\_seen\_at: string

The RFC3339 timestamp when the registration was last seen.

<a href="#">Link to this property</a>

<details>

<summary>

registration\_type: "warp"or "browser\_extension"

The registration client type, derived from device\_type.

</summary>

One of the following:

"warp"

<a href="#">Link to this property</a>

"browser\_extension"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp when the registration was last updated.

<a href="#">Link to this property</a>

deleted\_at: optional string

The RFC3339 timestamp when the registration was deleted.

<a href="#">Link to this property</a>

key\_type: optional string

The type of encryption key used by the WARP client for the active key. Currently ‘curve25519’ for WireGuard and ‘secp256r1’ for MASQUE.

<a href="#">Link to this property</a>

<details>

<summary>

policy: optional object {id, default, deleted, 2 more }

The device settings profile assigned to this registration.

</summary>

id: string

The ID of the device settings profile.

<a href="#">Link to this property</a>

default: boolean

Whether the device settings profile is the default profile for the account.

<a href="#">Link to this property</a>

deleted: boolean

Whether the device settings profile was deleted.

<a href="#">Link to this property</a>

name: string

The name of the device settings profile.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339 timestamp of when the device settings profile last changed for the registration.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

revoked\_at: optional string

The RFC3339 timestamp when the registration was revoked.

<a href="#">Link to this property</a>

tunnel\_type: optional string

Type of the tunnel - wireguard or masque.

<a href="#">Link to this property</a>

<details>

<summary>

user: optional object {id, email, name }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

email: optional string

The contact email address of the user.

maxLength90

<a href="#">Link to this property</a>

name: optional string

The enrolled device user’s name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

virtual\_ipv4: optional string

The virtual IPv4 address assigned to the network interface of the tunnel for this registration.

<a href="#">Link to this property</a>

virtual\_ipv6: optional string

The virtual IPv6 address assigned to the network interface of the tunnel for this registration.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_get_response%20%3E%20(schema)>)

RegistrationDeleteResponse = unknown

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_delete_response%20%3E%20(schema)>)

RegistrationBulkDeleteResponse = unknown

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_bulk_delete_response%20%3E%20(schema)>)

RegistrationRevokeResponse = unknown

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_revoke_response%20%3E%20(schema)>)

RegistrationUnrevokeResponse = unknown

[Link to this property](#)%20zero_trust.devices.registrations%20%3E%20(model)%20registration_unrevoke_response%20%3E%20(schema)>)

#### Zero TrustDevicesDEX Tests

##### [List Device DEX tests](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/dex_tests/methods/list)

GET/accounts/{account\_id}/dex/devices/dex\_tests

##### [Get Device DEX test](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/dex_tests/methods/get)

GET/accounts/{account\_id}/dex/devices/dex\_tests/{dex\_test\_id}

##### [Create Device DEX test](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/dex_tests/methods/create)

POST/accounts/{account\_id}/dex/devices/dex\_tests

##### [Update Device DEX test](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/dex_tests/methods/update)

PUT/accounts/{account\_id}/dex/devices/dex\_tests/{dex\_test\_id}

##### [Delete Device DEX test](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/dex_tests/methods/delete)

DELETE/accounts/{account\_id}/dex/devices/dex\_tests/{dex\_test\_id}

##### ModelsExpand Collapse

<details>

<summary>

SchemaData object {host, kind, method }

The configuration object which contains the details for the WARP client to conduct the test.

</summary>

host: string

The desired endpoint to test.

<a href="#">Link to this property</a>

<details>

<summary>

kind: "http"or "traceroute"

The type of test.

</summary>

One of the following:

"http"

<a href="#">Link to this property</a>

"traceroute"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

method: optional "GET"

The HTTP request method type.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.dex_tests%20%3E%20(model)%20schema_data%20%3E%20(schema)>)

<details>

<summary>

SchemaHTTP object {data, enabled, interval, 7 more }

</summary>

data: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.dex_tests%20%3E%20(model)%20schema_data%20%3E%20(schema)">SchemaData</a> { host, kind, method }

The configuration object which contains the details for the WARP client to conduct the test.

<a href="#">Link to this property</a>

enabled: boolean

Determines whether or not the test is active.

<a href="#">Link to this property</a>

interval: string

How often the test will run.

<a href="#">Link to this property</a>

name: string

The name of the DEX test. Must be unique.

<a href="#">Link to this property</a>

created: optional string

Date the test was created, in RFC 3339 format.

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Additional details about the test.

<a href="#">Link to this property</a>

<details>

<summary>

target\_policies: optional array of object {id, default, name }

DEX rules targeted by this test

</summary>

id: string

The id of the DEX rule.

maxLength36

<a href="#">Link to this property</a>

default: optional boolean

Whether the DEX rule is the account default.

<a href="#">Link to this property</a>

name: optional string

The name of the DEX rule.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

targeted: optional boolean

<a href="#">Link to this property</a>

test\_id: optional string

The unique identifier for the test.

maxLength32

<a href="#">Link to this property</a>

updated: optional string

Date the test was last updated, in RFC 3339 format.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.dex_tests%20%3E%20(model)%20schema_http%20%3E%20(schema)>)

<details>

<summary>

DEXTestDeleteResponse object {dex\_tests }

</summary>

<details>

<summary>

dex\_tests: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.dex_tests%20%3E%20(model)%20schema_http%20%3E%20(schema)">SchemaHTTP</a> { data, enabled, interval, 7 more }

</summary>

data: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.dex_tests%20%3E%20(model)%20schema_data%20%3E%20(schema)">SchemaData</a> { host, kind, method }

The configuration object which contains the details for the WARP client to conduct the test.

<a href="#">Link to this property</a>

enabled: boolean

Determines whether or not the test is active.

<a href="#">Link to this property</a>

interval: string

How often the test will run.

<a href="#">Link to this property</a>

name: string

The name of the DEX test. Must be unique.

<a href="#">Link to this property</a>

created: optional string

Date the test was created, in RFC 3339 format.

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Additional details about the test.

<a href="#">Link to this property</a>

<details>

<summary>

target\_policies: optional array of object {id, default, name }

DEX rules targeted by this test

</summary>

id: string

The id of the DEX rule.

maxLength36

<a href="#">Link to this property</a>

default: optional boolean

Whether the DEX rule is the account default.

<a href="#">Link to this property</a>

name: optional string

The name of the DEX rule.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

targeted: optional boolean

<a href="#">Link to this property</a>

test\_id: optional string

The unique identifier for the test.

maxLength32

<a href="#">Link to this property</a>

updated: optional string

Date the test was last updated, in RFC 3339 format.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.dex_tests%20%3E%20(model)%20dex_test_delete_response%20%3E%20(schema)>)

#### Zero TrustDevicesIP Profiles

##### [List IP profiles](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/ip_profiles/methods/list)

GET/accounts/{account\_id}/devices/ip-profiles

##### [Get IP profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/ip_profiles/methods/get)

GET/accounts/{account\_id}/devices/ip-profiles/{profile\_id}

##### [Create IP profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/ip_profiles/methods/create)

POST/accounts/{account\_id}/devices/ip-profiles

##### [Update IP profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/ip_profiles/methods/update)

PATCH/accounts/{account\_id}/devices/ip-profiles/{profile\_id}

##### [Delete IP profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/ip_profiles/methods/delete)

DELETE/accounts/{account\_id}/devices/ip-profiles/{profile\_id}

##### ModelsExpand Collapse

<details>

<summary>

IPProfile object {id, created\_at, description, 6 more }

</summary>

id: string

The ID of the Device IP profile.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339Nano timestamp when the Device IP profile was created.

<a href="#">Link to this property</a>

description: string

An optional description of the Device IP profile.

<a href="#">Link to this property</a>

enabled: boolean

Whether the Device IP profile is enabled.

<a href="#">Link to this property</a>

match: string

The wirefilter expression to match registrations. Available values: “identity.name”, “identity.email”, “identity.groups.id”, “identity.groups.name”, “identity.groups.email”, “identity.saml\_attributes”.

maxLength10000

<a href="#">Link to this property</a>

name: string

A user-friendly name for the Device IP profile.

<a href="#">Link to this property</a>

precedence: number

The precedence of the Device IP profile. Lower values indicate higher precedence. Device IP profile will be evaluated in ascending order of this field.

<a href="#">Link to this property</a>

subnet\_id: string

The ID of the Subnet.

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339Nano timestamp when the Device IP profile was last updated.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.ip_profiles%20%3E%20(model)%20ip_profile%20%3E%20(schema)>)

<details>

<summary>

IPProfileDeleteResponse object {id }

</summary>

id: optional string

ID of the deleted Device IP profile.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.ip_profiles%20%3E%20(model)%20ip_profile_delete_response%20%3E%20(schema)>)

#### Zero TrustDevicesDeployment Groups

##### [List deployment groups](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/deployment_groups/methods/list)

GET/accounts/{account\_id}/devices/deployment-groups

##### [Get deployment group](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/deployment_groups/methods/get)

GET/accounts/{account\_id}/devices/deployment-groups/{group\_id}

##### [Create deployment group](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/deployment_groups/methods/create)

POST/accounts/{account\_id}/devices/deployment-groups

##### [Update deployment group](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/deployment_groups/methods/edit)

PATCH/accounts/{account\_id}/devices/deployment-groups/{group\_id}

##### [Delete deployment group](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/deployment_groups/methods/delete)

DELETE/accounts/{account\_id}/devices/deployment-groups/{group\_id}

##### ModelsExpand Collapse

<details>

<summary>

DeploymentGroup object {id, created\_at, name, 3 more }

</summary>

id: string

The ID of the deployment group.

<a href="#">Link to this property</a>

created\_at: string

The RFC3339Nano timestamp when the deployment group was created.

<a href="#">Link to this property</a>

name: string

A user-friendly name for the deployment group.

maxLength255

minLength1

<a href="#">Link to this property</a>

updated\_at: string

The RFC3339Nano timestamp when the deployment group was last updated.

<a href="#">Link to this property</a>

<details>

<summary>

version\_config: array of object {target\_environment, version }

Contains version configurations for different target environments.

</summary>

target\_environment: string

The target environment for the client version (e.g., windows, macos).

<a href="#">Link to this property</a>

version: string

The specific client version to deploy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

policy\_ids: optional array of string

Contains a list of policy IDs assigned to this deployment group.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.deployment_groups%20%3E%20(model)%20deployment_group%20%3E%20(schema)>)

<details>

<summary>

DeploymentGroupDeleteResponse object {id }

</summary>

id: optional string

The ID of a deleted deployment group.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.deployment_groups%20%3E%20(model)%20deployment_group_delete_response%20%3E%20(schema)>)

#### Zero TrustDevicesNetworks

##### [List your device managed networks](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/networks/methods/list)

GET/accounts/{account\_id}/devices/networks

##### [Get device managed network details](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/networks/methods/get)

GET/accounts/{account\_id}/devices/networks/{network\_id}

##### [Create a device managed network](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/networks/methods/create)

POST/accounts/{account\_id}/devices/networks

##### [Update a device managed network](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/networks/methods/update)

PUT/accounts/{account\_id}/devices/networks/{network\_id}

##### [Delete a device managed network](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/networks/methods/delete)

DELETE/accounts/{account\_id}/devices/networks/{network\_id}

##### ModelsExpand Collapse

<details>

<summary>

DeviceNetwork object {config, name, network\_id, type }

</summary>

<details>

<summary>

config: optional object {tls\_sockaddr, sha256 }

The configuration object containing information for the WARP client to detect the managed network.

</summary>

tls\_sockaddr: string

A network address of the form “host:port” that the WARP client will use to detect the presence of a TLS host.

<a href="#">Link to this property</a>

sha256: optional string

The SHA-256 hash of the TLS certificate presented by the host found at tls\_sockaddr. If absent, regular certificate verification (trusted roots, valid timestamp, etc) will be used to validate the certificate.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The name of the device managed network. This name must be unique.

<a href="#">Link to this property</a>

network\_id: optional string

API UUID.

maxLength36

<a href="#">Link to this property</a>

type: optional "tls"

The type of device managed network.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.networks%20%3E%20(model)%20device_network%20%3E%20(schema)>)

#### Zero TrustDevicesFleet Status

##### [Get the latest status of a device.](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/fleet_status/methods/get)

GET/accounts/{account\_id}/dex/devices/{device\_id}/fleet-status/live

##### ModelsExpand Collapse

<details>

<summary>

FleetStatusGetResponse object {colo, deviceId, mode, 40 more }

</summary>

colo: string

Cloudflare colo airport code.

<a href="#">Link to this property</a>

deviceId: string

Device identifier (UUID v4)

<a href="#">Link to this property</a>

mode: string

The mode under which the WARP client is run.

<a href="#">Link to this property</a>

platform: string

Operating system.

<a href="#">Link to this property</a>

status: string

Network status.

<a href="#">Link to this property</a>

timestamp: string

<a href="#">Link to this property</a>

version: string

WARP client version.

<a href="#">Link to this property</a>

alwaysOn: optional boolean

<a href="#">Link to this property</a>

batteryCharging: optional boolean

<a href="#">Link to this property</a>

batteryCycles: optional number

formatint64

<a href="#">Link to this property</a>

batteryPct: optional number

formatfloat

<a href="#">Link to this property</a>

connectionType: optional string

<a href="#">Link to this property</a>

cpuPct: optional number

formatfloat

<a href="#">Link to this property</a>

<details>

<summary>

cpuPctByApp: optional array of object {cpu\_pct, name }

</summary>

cpu\_pct: optional number

CPU usage percentage, on a scale of 0 to 100.

formatfloat

maximum100

minimum0

<a href="#">Link to this property</a>

name: optional string

Application name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

deviceIpv4: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

deviceIpv6: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deviceName: optional string

Device identifier (human readable).

<a href="#">Link to this property</a>

DeprecateddeviceRegistration: optional string

Use <code>registrationId</code> instead.

Deprecated: use registrationId. Device registration identifier (UUID).

<a href="#">Link to this property</a>

diskReadBps: optional number

formatint64

<a href="#">Link to this property</a>

diskUsagePct: optional number

formatfloat

<a href="#">Link to this property</a>

diskWriteBps: optional number

formatint64

<a href="#">Link to this property</a>

dohSubdomain: optional string

<a href="#">Link to this property</a>

estimatedLossPct: optional number

formatfloat

<a href="#">Link to this property</a>

firewallEnabled: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

gatewayIpv4: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

gatewayIpv6: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handshakeLatencyMs: optional number

formatint64

<a href="#">Link to this property</a>

<details>

<summary>

ispIpv4: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ispIpv6: optional object {address, asn, aso, 4 more }

</summary>

address: optional string

<a href="#">Link to this property</a>

asn: optional number

<a href="#">Link to this property</a>

aso: optional string

<a href="#">Link to this property</a>

<details>

<summary>

location: optional object {city, country\_iso, state\_iso, zip }

</summary>

city: optional string

<a href="#">Link to this property</a>

country\_iso: optional string

<a href="#">Link to this property</a>

state\_iso: optional string

<a href="#">Link to this property</a>

zip: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

netmask: optional string

<a href="#">Link to this property</a>

version: optional number

IP version (<code>1</code> for IPv4, <code>2</code> for IPv6, <code>0</code> if unknown).

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

metal: optional string

<a href="#">Link to this property</a>

networkRcvdBps: optional number

formatint64

<a href="#">Link to this property</a>

networkSentBps: optional number

formatint64

<a href="#">Link to this property</a>

networkSsid: optional string

<a href="#">Link to this property</a>

personEmail: optional string

User contact email address

<a href="#">Link to this property</a>

ramAvailableKb: optional number

formatint64

<a href="#">Link to this property</a>

ramUsedPct: optional number

formatfloat

<a href="#">Link to this property</a>

<details>

<summary>

ramUsedPctByApp: optional array of object {name, ram\_used\_pct }

</summary>

name: optional string

Application name.

<a href="#">Link to this property</a>

ram\_used\_pct: optional number

RAM usage percentage, on a scale of 0 to 100.

formatfloat

maximum100

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

registrationId: optional string

Device registration identifier (UUID v4). On multi-user devices, this uniquely identifies a user’s registration on the device.

<a href="#">Link to this property</a>

<details>

<summary>

rtt: optional object {minRttUs, rttUs, rttVarUs }

Round-trip time statistics for the WARP tunnel.

</summary>

<details>

<summary>

minRttUs: optional object {downstream, upstream }

Minimum round-trip time in microseconds.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rttUs: optional object {downstream, upstream }

Round-trip time in microseconds.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rttVarUs: optional object {downstream, upstream }

Round-trip time variance in microseconds.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

switchLocked: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

tunnelStats: optional object {bytesLost, bytesReceived, bytesRetransmitted, 6 more }

WARP tunnel packet and byte counters.

</summary>

<details>

<summary>

bytesLost: optional object {downstream, upstream }

Number of bytes lost, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

bytesReceived: optional object {downstream, upstream }

Number of bytes received, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

bytesRetransmitted: optional object {downstream, upstream }

Number of bytes retransmitted, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

bytesSent: optional object {downstream, upstream }

Number of bytes sent, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packetsLost: optional object {downstream, upstream }

Number of packets lost, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packetsReceived: optional object {downstream, upstream }

Number of packets received, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packetsRetransmitted: optional object {downstream, upstream }

Number of packets retransmitted, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packetsSent: optional object {downstream, upstream }

Number of packets sent, split by direction.

</summary>

downstream: optional number

<a href="#">Link to this property</a>

upstream: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statsWindowMs: optional number

The measurement window duration in milliseconds.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tunnelType: optional string

<a href="#">Link to this property</a>

wifiStrengthDbm: optional number

formatint64

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.fleet_status%20%3E%20(model)%20fleet_status_get_response%20%3E%20(schema)>)

#### Zero TrustDevicesPolicies

##### ModelsExpand Collapse

<details>

<summary>

DevicePolicyCertificates object {enabled }

</summary>

enabled: boolean

The current status of the device policy certificate provisioning feature for WARP clients.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies%20%3E%20(model)%20device_policy_certificates%20%3E%20(schema)>)

<details>

<summary>

FallbackDomain object {suffix, description, dns\_server }

</summary>

suffix: string

The domain suffix to match when resolving locally.

<a href="#">Link to this property</a>

description: optional string

A description of the fallback domain, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

dns\_server: optional array of string

A list of IP addresses to handle domain resolution.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies%20%3E%20(model)%20fallback_domain%20%3E%20(schema)>)

<details>

<summary>

SettingsPolicy object {allow\_mode\_switch, allow\_updates, allowed\_to\_leave, 30 more }

</summary>

allow\_mode\_switch: optional boolean

Whether to allow the user to switch WARP between modes.

<a href="#">Link to this property</a>

allow\_updates: optional boolean

Whether to receive update notifications when a new version of the client is available.

<a href="#">Link to this property</a>

allowed\_to\_leave: optional boolean

Whether to allow devices to leave the organization.

<a href="#">Link to this property</a>

auto\_connect: optional number

The amount of time in seconds to reconnect after having been disabled.

<a href="#">Link to this property</a>

<details>

<summary>

browser\_extension\_config: optional object {proxy\_control, proxy\_enabled }

Browser extension proxy settings. Required when profile\_type is browser\_extension and invalid for WARP profiles.

</summary>

<details>

<summary>

proxy\_control: "unlocked"or "locked"

Whether the user may disable the browser extension proxy.

</summary>

One of the following:

"unlocked"

<a href="#">Link to this property</a>

"locked"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

proxy\_enabled: boolean

Whether the browser extension proxy is active.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

captive\_portal: optional number

Turn on the captive portal after the specified amount of time.

<a href="#">Link to this property</a>

default: optional boolean

Whether the policy is the account default. WARP group profiles cannot set this field.

<a href="#">Link to this property</a>

description: optional string

A description of the policy.

maxLength500

<a href="#">Link to this property</a>

disable\_auto\_fallback: optional boolean

If the <code>dns_server</code> field of a fallback domain is not present, the client will fall back to a best guess of the default/system DNS resolvers unless this policy option is set to <code>true</code>.

<a href="#">Link to this property</a>

<details>

<summary>

dns\_search\_suffixes: optional array of object {suffix, description }

List of DNS search suffixes to apply to clients. Suffixes are evaluated in order. Use an empty array to clear.

</summary>

suffix: string

The DNS search suffix to append when resolving short hostnames.

<a href="#">Link to this property</a>

description: optional string

A description of the DNS search suffix.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the policy will be applied to matching devices.

<a href="#">Link to this property</a>

<details>

<summary>

exclude: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_exclude%20%3E%20(schema)">SplitTunnelExclude</a>

List of routes excluded in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to exclude from the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to exclude from the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

exclude\_office\_ips: optional boolean

Whether to add Microsoft IPs to Split Tunnel exclusions.

<a href="#">Link to this property</a>

<details>

<summary>

fallback\_domains: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20fallback_domain%20%3E%20(schema)">FallbackDomain</a> { suffix, description, dns\_server }

</summary>

suffix: string

The domain suffix to match when resolving locally.

<a href="#">Link to this property</a>

description: optional string

A description of the fallback domain, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

dns\_server: optional array of string

A list of IP addresses to handle domain resolution.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

gateway\_unique\_id: optional string

<a href="#">Link to this property</a>

<details>

<summary>

global\_acceleration: optional object {api\_endpoints, enabled, masque\_endpoints, 2 more }

Global Acceleration settings for China. When configured, WARP clients connect to the Global Accelerator addresses instead of the default ones. Please contact your account representative to enable this feature on your account. See <a href="https://developers.cloudflare.com/china-network/concepts/global-acceleration/">https://developers.cloudflare.com/china-network/concepts/global-acceleration/</a>.

</summary>

api\_endpoints: array of string

IP:port entries for the API endpoints.

<a href="#">Link to this property</a>

enabled: boolean

Global acceleration settings are used only when “enabled”.

<a href="#">Link to this property</a>

masque\_endpoints: array of string

IP:port entries for the MASQUE tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

wireguard\_endpoints: array of string

IP:port entries for the WireGuard tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

autoswitch: optional boolean

Automatically switch Global Acceleration regions based on device location. Defaults to false when not provided.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

include: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_include%20%3E%20(schema)">SplitTunnelInclude</a>

List of routes included in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to include in the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to include in the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

lan\_allow\_minutes: optional number

The amount of time in minutes a user is allowed access to their LAN. A value of 0 will allow LAN access until the next WARP reconnection, such as a reboot or a laptop waking from sleep. Note that this field is omitted from the response if null or unset.

<a href="#">Link to this property</a>

lan\_allow\_subnet\_size: optional number

The size of the subnet for the local access network. Note that this field is omitted from the response if null or unset.

<a href="#">Link to this property</a>

match: optional string

The wirefilter expression to match devices. Available values: “identity.email”, “identity.groups.id”, “identity.groups.name”, “identity.groups.email”, “identity.service\_token\_uuid”, “identity.saml\_attributes”, “network”, “os.name”, “os.version”.

maxLength500

<a href="#">Link to this property</a>

name: optional string

The name of the device settings profile.

maxLength100

<a href="#">Link to this property</a>

policy\_id: optional string

maxLength36

<a href="#">Link to this property</a>

precedence: optional number

The precedence of the policy. Lower values indicate higher precedence. Policies will be evaluated in ascending order of this field.

<a href="#">Link to this property</a>

<details>

<summary>

profile\_type: optional "warp"or "browser\_extension"

The client type to which the device settings profile applies. This field is set when the profile is created and cannot be changed.

</summary>

One of the following:

"warp"

<a href="#">Link to this property</a>

"browser\_extension"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

register\_interface\_ip\_with\_dns: optional boolean

Determines if the operating system will register WARP’s local interface IP with your on-premises DNS server.

<a href="#">Link to this property</a>

sccm\_vpn\_boundary\_support: optional boolean

Determines whether the WARP client indicates to SCCM that it is inside a VPN boundary. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

service\_mode\_v2: optional object {mode, port }

</summary>

mode: optional string

The mode to run the WARP client under.

<a href="#">Link to this property</a>

port: optional number

The port number when used with proxy mode.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_url: optional string

The URL to launch when the Send Feedback button is clicked.

<a href="#">Link to this property</a>

switch\_locked: optional boolean

Whether to allow the user to turn off the WARP switch and disconnect the client.

<a href="#">Link to this property</a>

<details>

<summary>

Deprecatedtarget\_tests: optional array of object {id, name }

</summary>

id: optional string

The id of the DEX test targeting this policy.

<a href="#">Link to this property</a>

name: optional string

The name of the DEX test targeting this policy.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tunnel\_protocol: optional string

Determines which tunnel protocol to use.

<a href="#">Link to this property</a>

uninstall\_protection: optional boolean

Determines whether uninstalling the WARP client requires an override code. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

virtual\_networks: optional object {allowed, default }

Virtual network access settings for the device.

</summary>

allowed: array of string

List of virtual network IDs the device is allowed to access. When virtual\_networks is set, at least one entry is required.

<a href="#">Link to this property</a>

default: string

The default virtual network ID. Must be included in the <code>allowed</code> list.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies%20%3E%20(model)%20settings_policy%20%3E%20(schema)>)

<details>

<summary>

SplitTunnelExclude = object {address, description } or object {host, description }

</summary>

One of the following:

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to exclude from the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to exclude from the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_exclude%20%3E%20(schema)>)

<details>

<summary>

SplitTunnelInclude = object {address, description } or object {host, description }

</summary>

One of the following:

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to include in the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to include in the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_include%20%3E%20(schema)>)

#### Zero TrustDevicesPoliciesDefault

##### [Get the default device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/methods/get)

GET/accounts/{account\_id}/devices/policy

##### [Update the default device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/methods/edit)

PATCH/accounts/{account\_id}/devices/policy

##### ModelsExpand Collapse

<details>

<summary>

DefaultGetResponse object {allow\_mode\_switch, allow\_updates, allowed\_to\_leave, 22 more }

</summary>

allow\_mode\_switch: optional boolean

Whether to allow the user to switch WARP between modes.

<a href="#">Link to this property</a>

allow\_updates: optional boolean

Whether to receive update notifications when a new version of the client is available.

<a href="#">Link to this property</a>

allowed\_to\_leave: optional boolean

Whether to allow devices to leave the organization.

<a href="#">Link to this property</a>

auto\_connect: optional number

The amount of time in seconds to reconnect after having been disabled.

<a href="#">Link to this property</a>

captive\_portal: optional number

Turn on the captive portal after the specified amount of time.

<a href="#">Link to this property</a>

default: optional boolean

Whether the policy will be applied to matching devices.

<a href="#">Link to this property</a>

disable\_auto\_fallback: optional boolean

If the <code>dns_server</code> field of a fallback domain is not present, the client will fall back to a best guess of the default/system DNS resolvers unless this policy option is set to <code>true</code>.

<a href="#">Link to this property</a>

<details>

<summary>

dns\_search\_suffixes: optional array of object {suffix, description }

List of DNS search suffixes to apply to clients. Suffixes are evaluated in order. Use an empty array to clear.

</summary>

suffix: string

The DNS search suffix to append when resolving short hostnames.

<a href="#">Link to this property</a>

description: optional string

A description of the DNS search suffix.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the policy will be applied to matching devices.

<a href="#">Link to this property</a>

<details>

<summary>

exclude: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_exclude%20%3E%20(schema)">SplitTunnelExclude</a>

List of routes excluded in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to exclude from the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to exclude from the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

exclude\_office\_ips: optional boolean

Whether to add Microsoft IPs to Split Tunnel exclusions.

<a href="#">Link to this property</a>

<details>

<summary>

fallback\_domains: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20fallback_domain%20%3E%20(schema)">FallbackDomain</a> { suffix, description, dns\_server }

</summary>

suffix: string

The domain suffix to match when resolving locally.

<a href="#">Link to this property</a>

description: optional string

A description of the fallback domain, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

dns\_server: optional array of string

A list of IP addresses to handle domain resolution.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

gateway\_unique\_id: optional string

<a href="#">Link to this property</a>

<details>

<summary>

global\_acceleration: optional object {api\_endpoints, enabled, masque\_endpoints, 2 more }

Global Acceleration settings for China. When configured, WARP clients connect to the Global Accelerator addresses instead of the default ones. Please contact your account representative to enable this feature on your account. See <a href="https://developers.cloudflare.com/china-network/concepts/global-acceleration/">https://developers.cloudflare.com/china-network/concepts/global-acceleration/</a>.

</summary>

api\_endpoints: array of string

IP:port entries for the API endpoints.

<a href="#">Link to this property</a>

enabled: boolean

Global acceleration settings are used only when “enabled”.

<a href="#">Link to this property</a>

masque\_endpoints: array of string

IP:port entries for the MASQUE tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

wireguard\_endpoints: array of string

IP:port entries for the WireGuard tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

autoswitch: optional boolean

Automatically switch Global Acceleration regions based on device location. Defaults to false when not provided.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

include: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_include%20%3E%20(schema)">SplitTunnelInclude</a>

List of routes included in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to include in the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to include in the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

policy\_id: optional string

maxLength36

<a href="#">Link to this property</a>

<details>

<summary>

profile\_type: optional "warp"or "browser\_extension"

The client type to which the device settings profile applies. This field is set when the profile is created and cannot be changed.

</summary>

One of the following:

"warp"

<a href="#">Link to this property</a>

"browser\_extension"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

register\_interface\_ip\_with\_dns: optional boolean

Determines if the operating system will register WARP’s local interface IP with your on-premises DNS server.

<a href="#">Link to this property</a>

sccm\_vpn\_boundary\_support: optional boolean

Determines whether the WARP client indicates to SCCM that it is inside a VPN boundary. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

service\_mode\_v2: optional object {mode, port }

</summary>

mode: optional string

The mode to run the WARP client under.

<a href="#">Link to this property</a>

port: optional number

The port number when used with proxy mode.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_url: optional string

The URL to launch when the Send Feedback button is clicked.

<a href="#">Link to this property</a>

switch\_locked: optional boolean

Whether to allow the user to turn off the WARP switch and disconnect the client.

<a href="#">Link to this property</a>

tunnel\_protocol: optional string

Determines which tunnel protocol to use.

<a href="#">Link to this property</a>

uninstall\_protection: optional boolean

Determines whether uninstalling the WARP client requires an override code. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

virtual\_networks: optional object {allowed, default }

Virtual network access settings for the device.

</summary>

allowed: array of string

List of virtual network IDs the device is allowed to access. When virtual\_networks is set, at least one entry is required.

<a href="#">Link to this property</a>

default: string

The default virtual network ID. Must be included in the <code>allowed</code> list.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies.default%20%3E%20(model)%20default_get_response%20%3E%20(schema)>)

<details>

<summary>

DefaultEditResponse object {allow\_mode\_switch, allow\_updates, allowed\_to\_leave, 22 more }

</summary>

allow\_mode\_switch: optional boolean

Whether to allow the user to switch WARP between modes.

<a href="#">Link to this property</a>

allow\_updates: optional boolean

Whether to receive update notifications when a new version of the client is available.

<a href="#">Link to this property</a>

allowed\_to\_leave: optional boolean

Whether to allow devices to leave the organization.

<a href="#">Link to this property</a>

auto\_connect: optional number

The amount of time in seconds to reconnect after having been disabled.

<a href="#">Link to this property</a>

captive\_portal: optional number

Turn on the captive portal after the specified amount of time.

<a href="#">Link to this property</a>

default: optional boolean

Whether the policy will be applied to matching devices.

<a href="#">Link to this property</a>

disable\_auto\_fallback: optional boolean

If the <code>dns_server</code> field of a fallback domain is not present, the client will fall back to a best guess of the default/system DNS resolvers unless this policy option is set to <code>true</code>.

<a href="#">Link to this property</a>

<details>

<summary>

dns\_search\_suffixes: optional array of object {suffix, description }

List of DNS search suffixes to apply to clients. Suffixes are evaluated in order. Use an empty array to clear.

</summary>

suffix: string

The DNS search suffix to append when resolving short hostnames.

<a href="#">Link to this property</a>

description: optional string

A description of the DNS search suffix.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the policy will be applied to matching devices.

<a href="#">Link to this property</a>

<details>

<summary>

exclude: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_exclude%20%3E%20(schema)">SplitTunnelExclude</a>

List of routes excluded in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to exclude from the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesExcludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to exclude from the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

exclude\_office\_ips: optional boolean

Whether to add Microsoft IPs to Split Tunnel exclusions.

<a href="#">Link to this property</a>

<details>

<summary>

fallback\_domains: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20fallback_domain%20%3E%20(schema)">FallbackDomain</a> { suffix, description, dns\_server }

</summary>

suffix: string

The domain suffix to match when resolving locally.

<a href="#">Link to this property</a>

description: optional string

A description of the fallback domain, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

dns\_server: optional array of string

A list of IP addresses to handle domain resolution.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

gateway\_unique\_id: optional string

<a href="#">Link to this property</a>

<details>

<summary>

global\_acceleration: optional object {api\_endpoints, enabled, masque\_endpoints, 2 more }

Global Acceleration settings for China. When configured, WARP clients connect to the Global Accelerator addresses instead of the default ones. Please contact your account representative to enable this feature on your account. See <a href="https://developers.cloudflare.com/china-network/concepts/global-acceleration/">https://developers.cloudflare.com/china-network/concepts/global-acceleration/</a>.

</summary>

api\_endpoints: array of string

IP:port entries for the API endpoints.

<a href="#">Link to this property</a>

enabled: boolean

Global acceleration settings are used only when “enabled”.

<a href="#">Link to this property</a>

masque\_endpoints: array of string

IP:port entries for the MASQUE tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

wireguard\_endpoints: array of string

IP:port entries for the WireGuard tunnel endpoints. Either wireguard\_endpoints or masque\_endpoints must be provided.

<a href="#">Link to this property</a>

autoswitch: optional boolean

Automatically switch Global Acceleration regions based on device location. Defaults to false when not provided.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

include: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.policies%20%3E%20(model)%20split_tunnel_include%20%3E%20(schema)">SplitTunnelInclude</a>

List of routes included in the WARP client’s tunnel.

</summary>

One of the following:

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithAddress object {address, description }

</summary>

address: string

The address in CIDR format to include in the tunnel. If <code>address</code> is present, <code>host</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesIncludeSplitTunnelWithHost object {host, description }

</summary>

host: string

The domain name to include in the tunnel. If <code>host</code> is present, <code>address</code> must not be present.

<a href="#">Link to this property</a>

description: optional string

A description of the Split Tunnel item, displayed in the client UI.

maxLength100

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

policy\_id: optional string

maxLength36

<a href="#">Link to this property</a>

<details>

<summary>

profile\_type: optional "warp"or "browser\_extension"

The client type to which the device settings profile applies. This field is set when the profile is created and cannot be changed.

</summary>

One of the following:

"warp"

<a href="#">Link to this property</a>

"browser\_extension"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

register\_interface\_ip\_with\_dns: optional boolean

Determines if the operating system will register WARP’s local interface IP with your on-premises DNS server.

<a href="#">Link to this property</a>

sccm\_vpn\_boundary\_support: optional boolean

Determines whether the WARP client indicates to SCCM that it is inside a VPN boundary. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

service\_mode\_v2: optional object {mode, port }

</summary>

mode: optional string

The mode to run the WARP client under.

<a href="#">Link to this property</a>

port: optional number

The port number when used with proxy mode.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_url: optional string

The URL to launch when the Send Feedback button is clicked.

<a href="#">Link to this property</a>

switch\_locked: optional boolean

Whether to allow the user to turn off the WARP switch and disconnect the client.

<a href="#">Link to this property</a>

tunnel\_protocol: optional string

Determines which tunnel protocol to use.

<a href="#">Link to this property</a>

uninstall\_protection: optional boolean

Determines whether uninstalling the WARP client requires an override code. (Windows only).

<a href="#">Link to this property</a>

<details>

<summary>

virtual\_networks: optional object {allowed, default }

Virtual network access settings for the device.

</summary>

allowed: array of string

List of virtual network IDs the device is allowed to access. When virtual\_networks is set, at least one entry is required.

<a href="#">Link to this property</a>

default: string

The default virtual network ID. Must be included in the <code>allowed</code> list.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.policies.default%20%3E%20(model)%20default_edit_response%20%3E%20(schema)>)

#### Zero TrustDevicesPoliciesDefaultExcludes

##### [Get the Split Tunnel exclude list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/excludes/methods/get)

GET/accounts/{account\_id}/devices/policy/exclude

##### [Set the Split Tunnel exclude list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/excludes/methods/update)

PUT/accounts/{account\_id}/devices/policy/exclude

#### Zero TrustDevicesPoliciesDefaultIncludes

##### [Get the Split Tunnel include list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/includes/methods/get)

GET/accounts/{account\_id}/devices/policy/include

##### [Set the Split Tunnel include list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/includes/methods/update)

PUT/accounts/{account\_id}/devices/policy/include

#### Zero TrustDevicesPoliciesDefaultFallback Domains

##### [Get your Local Domain Fallback list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/fallback_domains/methods/get)

GET/accounts/{account\_id}/devices/policy/fallback\_domains

##### [Set your Local Domain Fallback list](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/fallback_domains/methods/update)

PUT/accounts/{account\_id}/devices/policy/fallback\_domains

#### Zero TrustDevicesPoliciesDefaultCertificates

##### [Get device certificate provisioning status](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/certificates/methods/get)

GET/zones/{zone\_id}/devices/policy/certificates

##### [Update device certificate provisioning status](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/default/subresources/certificates/methods/edit)

PATCH/zones/{zone\_id}/devices/policy/certificates

#### Zero TrustDevicesPoliciesCustom

##### [List device settings profiles](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/methods/list)

GET/accounts/{account\_id}/devices/policies

##### [Get device settings profile by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/methods/get)

GET/accounts/{account\_id}/devices/policy/{policy\_id}

##### [Create a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/methods/create)

POST/accounts/{account\_id}/devices/policy

##### [Update a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/methods/edit)

PATCH/accounts/{account\_id}/devices/policy/{policy\_id}

##### [Delete a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/methods/delete)

DELETE/accounts/{account\_id}/devices/policy/{policy\_id}

#### Zero TrustDevicesPoliciesCustomExcludes

##### [Get the Split Tunnel exclude list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/excludes/methods/get)

GET/accounts/{account\_id}/devices/policy/{policy\_id}/exclude

##### [Set the Split Tunnel exclude list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/excludes/methods/update)

PUT/accounts/{account\_id}/devices/policy/{policy\_id}/exclude

#### Zero TrustDevicesPoliciesCustomIncludes

##### [Get the Split Tunnel include list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/includes/methods/get)

GET/accounts/{account\_id}/devices/policy/{policy\_id}/include

##### [Set the Split Tunnel include list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/includes/methods/update)

PUT/accounts/{account\_id}/devices/policy/{policy\_id}/include

#### Zero TrustDevicesPoliciesCustomFallback Domains

##### [Get the Local Domain Fallback list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/fallback_domains/methods/get)

GET/accounts/{account\_id}/devices/policy/{policy\_id}/fallback\_domains

##### [Set the Local Domain Fallback list for a device settings profile](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/policies/subresources/custom/subresources/fallback_domains/methods/update)

PUT/accounts/{account\_id}/devices/policy/{policy\_id}/fallback\_domains

#### Zero TrustDevicesPosture

##### [List posture rules](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/methods/list)

GET/accounts/{account\_id}/devices/posture

##### [Get posture rule](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/methods/get)

GET/accounts/{account\_id}/devices/posture/{rule\_id}

##### [Create posture rule](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/methods/create)

POST/accounts/{account\_id}/devices/posture

##### [Update posture rule](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/methods/update)

PUT/accounts/{account\_id}/devices/posture/{rule\_id}

##### [Delete posture rule](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/methods/delete)

DELETE/accounts/{account\_id}/devices/posture/{rule\_id}

##### ModelsExpand Collapse

CarbonblackInput = string

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20carbonblack_input%20%3E%20(schema)>)

<details>

<summary>

ClientCertificateInput object {certificate\_id, cn }

</summary>

certificate\_id: string

UUID of Cloudflare managed certificate.

maxLength36

<a href="#">Link to this property</a>

cn: string

Common Name that is protected by the certificate.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20client_certificate_input%20%3E%20(schema)>)

<details>

<summary>

CrowdstrikeInput object {connection\_id, last\_seen, operator, 6 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

last\_seen: optional string

For more details on last seen, please refer to the Crowdstrike documentation.

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

os: optional string

Os Version.

<a href="#">Link to this property</a>

overall: optional string

Overall.

<a href="#">Link to this property</a>

sensor\_config: optional string

SensorConfig.

<a href="#">Link to this property</a>

<details>

<summary>

state: optional "online"or "offline"or "unknown"

For more details on state, please refer to the Crowdstrike documentation.

</summary>

One of the following:

"online"

<a href="#">Link to this property</a>

"offline"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: optional string

Version.

<a href="#">Link to this property</a>

<details>

<summary>

versionOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Version Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20crowdstrike_input%20%3E%20(schema)>)

<details>

<summary>

DeviceInput = <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20file_input%20%3E%20(schema)">FileInput</a> { operating\_system, path, exists, 2 more } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20unique_client_id_input%20%3E%20(schema)">UniqueClientIDInput</a> { id, operating\_system } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20domain_joined_input%20%3E%20(schema)">DomainJoinedInput</a> { operating\_system, domain } or 17 more

The value to be checked against.

</summary>

One of the following:

<details>

<summary>

FileInput object {operating\_system, path, exists, 2 more }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

File path.

<a href="#">Link to this property</a>

exists: optional boolean

Whether or not file exists.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

UniqueClientIDInput object {id, operating\_system }

</summary>

id: string

List ID.

<a href="#">Link to this property</a>

<details>

<summary>

operating\_system: "android"or "ios"or "chromeos"

Operating System.

</summary>

One of the following:

"android"

<a href="#">Link to this property</a>

"ios"

<a href="#">Link to this property</a>

"chromeos"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainJoinedInput object {operating\_system, domain }

</summary>

operating\_system: "windows"

Operating System.

<a href="#">Link to this property</a>

domain: optional string

Domain.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OSVersionInput object {operating\_system, operator, version, 3 more }

</summary>

operating\_system: "windows"

Operating System.

<a href="#">Link to this property</a>

<details>

<summary>

operator: "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: string

Version of OS.

<a href="#">Link to this property</a>

os\_distro\_name: optional string

Operating System Distribution Name (linux only).

<a href="#">Link to this property</a>

os\_distro\_revision: optional string

Version of OS Distribution (linux only).

<a href="#">Link to this property</a>

os\_version\_extra: optional string

Additional operating system version details. For Windows, the UBR (Update Build Revision). For Mac or iOS, the Product Version Extra. For Linux, the distribution name and version.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

FirewallInput object {enabled, operating\_system }

</summary>

enabled: boolean

Enabled.

<a href="#">Link to this property</a>

<details>

<summary>

operating\_system: "windows"or "mac"

Operating System.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SentineloneInput object {operating\_system, path, sha256, thumbprint }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

File path.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesCarbonblackInputRequest object {operating\_system, path, sha256, thumbprint }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

File path.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesAccessSerialNumberListInputRequest object {id }

</summary>

id: string

UUID of Access List.

maxLength36

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DiskEncryptionInput object {checkDisks, requireAll }

</summary>

checkDisks: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20carbonblack_input%20%3E%20(schema)">CarbonblackInput</a>

List of volume names to be checked for encryption.

<a href="#">Link to this property</a>

requireAll: optional boolean

Whether to check all disks for encryption.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesApplicationInputRequest object {operating\_system, path, sha256, thumbprint }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

Path for the application.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ClientCertificateInput object {certificate\_id, cn }

</summary>

certificate\_id: string

UUID of Cloudflare managed certificate.

maxLength36

<a href="#">Link to this property</a>

cn: string

Common Name that is protected by the certificate.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesClientCertificateV2InputRequest object {certificate\_id, check\_private\_key, operating\_system, 4 more }

</summary>

certificate\_id: string

UUID of Cloudflare managed certificate.

maxLength36

<a href="#">Link to this property</a>

check\_private\_key: boolean

Confirm the certificate was not imported from another device. We recommend keeping this enabled unless the certificate was deployed without a private key.

<a href="#">Link to this property</a>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

cn: optional string

Certificate Common Name. This may include one or more variables in the ${ } notation. Only ${serial\_number} and ${hostname} are valid variables.

<a href="#">Link to this property</a>

<details>

<summary>

extended\_key\_usage: optional array of "clientAuth"or "emailProtection"

List of values indicating purposes for which the certificate public key can be used.

</summary>

One of the following:

"clientAuth"

<a href="#">Link to this property</a>

"emailProtection"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

locations: optional object {paths, trust\_stores }

</summary>

paths: optional array of string

List of paths to check for client certificate on linux.

<a href="#">Link to this property</a>

<details>

<summary>

trust\_stores: optional array of "system"or "user"

List of trust stores to check for client certificate.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"user"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

subject\_alternative\_names: optional array of string

List of certificate Subject Alternative Names.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesAntivirusInputRequest object {update\_window\_days }

</summary>

update\_window\_days: optional number

Number of days that the antivirus should be updated within.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

WorkspaceOneInput object {compliance\_status, connection\_id }

</summary>

<details>

<summary>

compliance\_status: "compliant"or "noncompliant"or "unknown"

Compliance Status.

</summary>

One of the following:

"compliant"

<a href="#">Link to this property</a>

"noncompliant"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CrowdstrikeInput object {connection\_id, last\_seen, operator, 6 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

last\_seen: optional string

For more details on last seen, please refer to the Crowdstrike documentation.

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

os: optional string

Os Version.

<a href="#">Link to this property</a>

overall: optional string

Overall.

<a href="#">Link to this property</a>

sensor\_config: optional string

SensorConfig.

<a href="#">Link to this property</a>

<details>

<summary>

state: optional "online"or "offline"or "unknown"

For more details on state, please refer to the Crowdstrike documentation.

</summary>

One of the following:

"online"

<a href="#">Link to this property</a>

"offline"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: optional string

Version.

<a href="#">Link to this property</a>

<details>

<summary>

versionOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Version Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IntuneInput object {compliance\_status, connection\_id }

</summary>

<details>

<summary>

compliance\_status: "compliant"or "noncompliant"or "unknown"or 3 more

Compliance Status.

</summary>

One of the following:

"compliant"

<a href="#">Link to this property</a>

"noncompliant"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

"notapplicable"

<a href="#">Link to this property</a>

"ingraceperiod"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

KolideInput object {connection\_id, auth\_state, countOperator, issue\_count }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_state: optional array of "Good"or "Notified"or "Will Block"or "Blocked"

The set of Kolide device authentication states that pass the posture check. Device must match one of the specified states.

</summary>

One of the following:

"Good"

<a href="#">Link to this property</a>

"Notified"

<a href="#">Link to this property</a>

"Will Block"

<a href="#">Link to this property</a>

"Blocked"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

countOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Count Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

issue\_count: optional string

The Number of Issues.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TaniumInput object {connection\_id, eid\_last\_seen, operator, 3 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

eid\_last\_seen: optional string

For more details on eid last seen, refer to the Tanium documentation.

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator to evaluate risk\_level or eid\_last\_seen.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: optional "low"or "medium"or "high"or "critical"

For more details on risk level, refer to the Tanium documentation.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"critical"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scoreOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Score Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

total\_score: optional number

For more details on total score, refer to the Tanium documentation.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SentineloneS2sInput object {connection\_id, active\_threats, infected, 4 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

active\_threats: optional number

The Number of active threats.

<a href="#">Link to this property</a>

infected: optional boolean

Whether device is infected.

<a href="#">Link to this property</a>

is\_active: optional boolean

Whether device is active.

<a href="#">Link to this property</a>

<details>

<summary>

network\_status: optional "connected"or "disconnected"or "disconnecting"or "connecting"

Network status of device.

</summary>

One of the following:

"connected"

<a href="#">Link to this property</a>

"disconnected"

<a href="#">Link to this property</a>

"disconnecting"

<a href="#">Link to this property</a>

"connecting"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

operational\_state: optional "na"or "partially\_disabled"or "auto\_fully\_disabled"or 4 more

Agent operational state.

</summary>

One of the following:

"na"

<a href="#">Link to this property</a>

"partially\_disabled"

<a href="#">Link to this property</a>

"auto\_fully\_disabled"

<a href="#">Link to this property</a>

"fully\_disabled"

<a href="#">Link to this property</a>

"auto\_partially\_disabled"

<a href="#">Link to this property</a>

"disabled\_error"

<a href="#">Link to this property</a>

"db\_corruption"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

TeamsDevicesCustomS2sInputRequest object {connection\_id, operator, score }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

<details>

<summary>

operator: "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

score: number

A value between 0-100 assigned to devices set by the 3rd party posture provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20device_input%20%3E%20(schema)>)

<details>

<summary>

DeviceMatch object {platform }

</summary>

<details>

<summary>

platform: optional "windows"or "mac"or "linux"or 3 more

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"android"

<a href="#">Link to this property</a>

"ios"

<a href="#">Link to this property</a>

"chromeos"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20device_match%20%3E%20(schema)>)

<details>

<summary>

DevicePostureRule object {id, description, enabled, 6 more }

</summary>

id: optional string

API UUID.

maxLength36

<a href="#">Link to this property</a>

description: optional string

The description of the device posture rule.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the rule is enabled. This is a computed, read-only value. It is false for deprecated Kolide posture rules that still use the issue\_count input, and true otherwise.

<a href="#">Link to this property</a>

expiration: optional string

Sets the expiration time for a posture check result. If empty, the result remains valid until it is overwritten by new data from the WARP client.

<a href="#">Link to this property</a>

input: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20device_input%20%3E%20(schema)">DeviceInput</a>

The value to be checked against.

<a href="#">Link to this property</a>

<details>

<summary>

match: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20device_match%20%3E%20(schema)">DeviceMatch</a> { platform }

The conditions that the client must match to run the rule.

</summary>

<details>

<summary>

platform: optional "windows"or "mac"or "linux"or 3 more

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"android"

<a href="#">Link to this property</a>

"ios"

<a href="#">Link to this property</a>

"chromeos"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The name of the device posture rule.

<a href="#">Link to this property</a>

schedule: optional string

Polling frequency for the WARP client posture check. Default: <code>5m</code> (poll every five minutes). Minimum: <code>1m</code>.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "file"or "application"or "tanium"or 20 more

The type of device posture rule.

</summary>

One of the following:

"file"

<a href="#">Link to this property</a>

"application"

<a href="#">Link to this property</a>

"tanium"

<a href="#">Link to this property</a>

"gateway"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"disk\_encryption"

<a href="#">Link to this property</a>

"serial\_number"

<a href="#">Link to this property</a>

"sentinelone"

<a href="#">Link to this property</a>

"carbonblack"

<a href="#">Link to this property</a>

"firewall"

<a href="#">Link to this property</a>

"os\_version"

<a href="#">Link to this property</a>

"domain\_joined"

<a href="#">Link to this property</a>

"client\_certificate"

<a href="#">Link to this property</a>

"client\_certificate\_v2"

<a href="#">Link to this property</a>

"antivirus"

<a href="#">Link to this property</a>

"unique\_client\_id"

<a href="#">Link to this property</a>

"kolide"

<a href="#">Link to this property</a>

"tanium\_s2s"

<a href="#">Link to this property</a>

"crowdstrike\_s2s"

<a href="#">Link to this property</a>

"intune"

<a href="#">Link to this property</a>

"workspace\_one"

<a href="#">Link to this property</a>

"sentinelone\_s2s"

<a href="#">Link to this property</a>

"custom\_s2s"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20device_posture_rule%20%3E%20(schema)>)

<details>

<summary>

DiskEncryptionInput object {checkDisks, requireAll }

</summary>

checkDisks: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.devices.posture%20%3E%20(model)%20carbonblack_input%20%3E%20(schema)">CarbonblackInput</a>

List of volume names to be checked for encryption.

<a href="#">Link to this property</a>

requireAll: optional boolean

Whether to check all disks for encryption.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20disk_encryption_input%20%3E%20(schema)>)

<details>

<summary>

DomainJoinedInput object {operating\_system, domain }

</summary>

operating\_system: "windows"

Operating System.

<a href="#">Link to this property</a>

domain: optional string

Domain.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20domain_joined_input%20%3E%20(schema)>)

<details>

<summary>

FileInput object {operating\_system, path, exists, 2 more }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

File path.

<a href="#">Link to this property</a>

exists: optional boolean

Whether or not file exists.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20file_input%20%3E%20(schema)>)

<details>

<summary>

FirewallInput object {enabled, operating\_system }

</summary>

enabled: boolean

Enabled.

<a href="#">Link to this property</a>

<details>

<summary>

operating\_system: "windows"or "mac"

Operating System.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20firewall_input%20%3E%20(schema)>)

<details>

<summary>

IntuneInput object {compliance\_status, connection\_id }

</summary>

<details>

<summary>

compliance\_status: "compliant"or "noncompliant"or "unknown"or 3 more

Compliance Status.

</summary>

One of the following:

"compliant"

<a href="#">Link to this property</a>

"noncompliant"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

"notapplicable"

<a href="#">Link to this property</a>

"ingraceperiod"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20intune_input%20%3E%20(schema)>)

<details>

<summary>

KolideInput object {connection\_id, auth\_state, countOperator, issue\_count }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_state: optional array of "Good"or "Notified"or "Will Block"or "Blocked"

The set of Kolide device authentication states that pass the posture check. Device must match one of the specified states.

</summary>

One of the following:

"Good"

<a href="#">Link to this property</a>

"Notified"

<a href="#">Link to this property</a>

"Will Block"

<a href="#">Link to this property</a>

"Blocked"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

countOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Count Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

issue\_count: optional string

The Number of Issues.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20kolide_input%20%3E%20(schema)>)

<details>

<summary>

OSVersionInput object {operating\_system, operator, version, 3 more }

</summary>

operating\_system: "windows"

Operating System.

<a href="#">Link to this property</a>

<details>

<summary>

operator: "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

version: string

Version of OS.

<a href="#">Link to this property</a>

os\_distro\_name: optional string

Operating System Distribution Name (linux only).

<a href="#">Link to this property</a>

os\_distro\_revision: optional string

Version of OS Distribution (linux only).

<a href="#">Link to this property</a>

os\_version\_extra: optional string

Additional operating system version details. For Windows, the UBR (Update Build Revision). For Mac or iOS, the Product Version Extra. For Linux, the distribution name and version.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20os_version_input%20%3E%20(schema)>)

<details>

<summary>

SentineloneInput object {operating\_system, path, sha256, thumbprint }

</summary>

<details>

<summary>

operating\_system: "windows"or "linux"or "mac"

Operating system.

</summary>

One of the following:

"windows"

<a href="#">Link to this property</a>

"linux"

<a href="#">Link to this property</a>

"mac"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

path: string

File path.

<a href="#">Link to this property</a>

sha256: optional string

SHA-256.

<a href="#">Link to this property</a>

thumbprint: optional string

Signing certificate thumbprint.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20sentinelone_input%20%3E%20(schema)>)

<details>

<summary>

SentineloneS2sInput object {connection\_id, active\_threats, infected, 4 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

active\_threats: optional number

The Number of active threats.

<a href="#">Link to this property</a>

infected: optional boolean

Whether device is infected.

<a href="#">Link to this property</a>

is\_active: optional boolean

Whether device is active.

<a href="#">Link to this property</a>

<details>

<summary>

network\_status: optional "connected"or "disconnected"or "disconnecting"or "connecting"

Network status of device.

</summary>

One of the following:

"connected"

<a href="#">Link to this property</a>

"disconnected"

<a href="#">Link to this property</a>

"disconnecting"

<a href="#">Link to this property</a>

"connecting"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

operational\_state: optional "na"or "partially\_disabled"or "auto\_fully\_disabled"or 4 more

Agent operational state.

</summary>

One of the following:

"na"

<a href="#">Link to this property</a>

"partially\_disabled"

<a href="#">Link to this property</a>

"auto\_fully\_disabled"

<a href="#">Link to this property</a>

"fully\_disabled"

<a href="#">Link to this property</a>

"auto\_partially\_disabled"

<a href="#">Link to this property</a>

"disabled\_error"

<a href="#">Link to this property</a>

"db\_corruption"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20sentinelone_s2s_input%20%3E%20(schema)>)

<details>

<summary>

TaniumInput object {connection\_id, eid\_last\_seen, operator, 3 more }

</summary>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

eid\_last\_seen: optional string

For more details on eid last seen, refer to the Tanium documentation.

<a href="#">Link to this property</a>

<details>

<summary>

operator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Operator to evaluate risk\_level or eid\_last\_seen.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: optional "low"or "medium"or "high"or "critical"

For more details on risk level, refer to the Tanium documentation.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"critical"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scoreOperator: optional "&lt;"or "&lt;="or "&gt;"or 2 more

Score Operator.

</summary>

One of the following:

"&lt;"

<a href="#">Link to this property</a>

"&lt;="

<a href="#">Link to this property</a>

"&gt;"

<a href="#">Link to this property</a>

"&gt;="

<a href="#">Link to this property</a>

"=="

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

total\_score: optional number

For more details on total score, refer to the Tanium documentation.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20tanium_input%20%3E%20(schema)>)

<details>

<summary>

UniqueClientIDInput object {id, operating\_system }

</summary>

id: string

List ID.

<a href="#">Link to this property</a>

<details>

<summary>

operating\_system: "android"or "ios"or "chromeos"

Operating System.

</summary>

One of the following:

"android"

<a href="#">Link to this property</a>

"ios"

<a href="#">Link to this property</a>

"chromeos"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20unique_client_id_input%20%3E%20(schema)>)

<details>

<summary>

WorkspaceOneInput object {compliance\_status, connection\_id }

</summary>

<details>

<summary>

compliance\_status: "compliant"or "noncompliant"or "unknown"

Compliance Status.

</summary>

One of the following:

"compliant"

<a href="#">Link to this property</a>

"noncompliant"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

connection\_id: string

Posture Integration ID.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20workspace_one_input%20%3E%20(schema)>)

<details>

<summary>

PostureDeleteResponse object {id }

</summary>

id: optional string

API UUID.

maxLength36

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture%20%3E%20(model)%20posture_delete_response%20%3E%20(schema)>)

#### Zero TrustDevicesPostureIntegrations

##### [List posture integrations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/subresources/integrations/methods/list)

GET/accounts/{account\_id}/devices/posture/integration

##### [Get posture integration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/subresources/integrations/methods/get)

GET/accounts/{account\_id}/devices/posture/integration/{integration\_id}

##### [Create posture integration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/subresources/integrations/methods/create)

POST/accounts/{account\_id}/devices/posture/integration

##### [Update posture integration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/subresources/integrations/methods/edit)

PATCH/accounts/{account\_id}/devices/posture/integration/{integration\_id}

##### [Delete posture integration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/posture/subresources/integrations/methods/delete)

DELETE/accounts/{account\_id}/devices/posture/integration/{integration\_id}

##### ModelsExpand Collapse

<details>

<summary>

Integration object {id, config, interval, 2 more }

</summary>

id: optional string

API UUID.

maxLength36

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {api\_url, auth\_url, client\_id }

The configuration object containing third-party integration information.

</summary>

api\_url: string

The Workspace One API URL provided in the Workspace One Admin Dashboard.

<a href="#">Link to this property</a>

auth\_url: string

The Workspace One Authorization URL depending on your region.

<a href="#">Link to this property</a>

client\_id: string

The Workspace One client ID provided in the Workspace One Admin Dashboard.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

interval: optional string

The interval between each posture check with the third-party API. Use <code>m</code> for minutes (e.g. <code>5m</code>) and <code>h</code> for hours (e.g. <code>12h</code>).

<a href="#">Link to this property</a>

name: optional string

The name of the device posture integration.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "workspace\_one"or "crowdstrike\_s2s"or "uptycs"or 5 more

The type of device posture integration.

</summary>

One of the following:

"workspace\_one"

<a href="#">Link to this property</a>

"crowdstrike\_s2s"

<a href="#">Link to this property</a>

"uptycs"

<a href="#">Link to this property</a>

"intune"

<a href="#">Link to this property</a>

"kolide"

<a href="#">Link to this property</a>

"tanium\_s2s"

<a href="#">Link to this property</a>

"sentinelone\_s2s"

<a href="#">Link to this property</a>

"custom\_s2s"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture.integrations%20%3E%20(model)%20integration%20%3E%20(schema)>)

<details>

<summary>

IntegrationDeleteResponse = unknownor string

</summary>

One of the following:

unknown

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.posture.integrations%20%3E%20(model)%20integration_delete_response%20%3E%20(schema)>)

#### Zero TrustDevicesRevoke

##### [Revoke devices (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/revoke/methods/create)

Deprecated

POST/accounts/{account\_id}/devices/revoke

##### ModelsExpand Collapse

<details>

<summary>

RevokeCreateResponse = unknownor string

</summary>

One of the following:

unknown

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.revoke%20%3E%20(model)%20revoke_create_response%20%3E%20(schema)>)

#### Zero TrustDevicesSettings

##### [Get device settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/settings/methods/get)

GET/accounts/{account\_id}/devices/settings

##### [Update device settings (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/settings/methods/update)

Deprecated

PUT/accounts/{account\_id}/devices/settings

##### [Update device settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/settings/methods/edit)

PATCH/accounts/{account\_id}/devices/settings

##### [Reset device settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/settings/methods/delete)

DELETE/accounts/{account\_id}/devices/settings

##### ModelsExpand Collapse

<details>

<summary>

DeviceSettings object {disable\_for\_time, external\_emergency\_signal\_enabled, external\_emergency\_signal\_fingerprint, 6 more }

</summary>

disable\_for\_time: optional number

Sets the time limit, in seconds, that a user can use an override code to bypass WARP.

<a href="#">Link to this property</a>

external\_emergency\_signal\_enabled: optional boolean

Controls whether the external emergency disconnect feature is enabled.

<a href="#">Link to this property</a>

external\_emergency\_signal\_fingerprint: optional string

The SHA256 fingerprint (64 hexadecimal characters) of the HTTPS server certificate for the external\_emergency\_signal\_url. If provided, the WARP client will use this value to verify the server’s identity. The device will ignore any response if the server’s certificate fingerprint does not exactly match this value.

<a href="#">Link to this property</a>

external\_emergency\_signal\_interval: optional string

The interval at which the WARP client fetches the emergency disconnect signal, formatted as a duration string (e.g., “5m”, “2m30s”, “1h”). Minimum 30 seconds.

<a href="#">Link to this property</a>

external\_emergency\_signal\_url: optional string

The HTTPS URL from which to fetch the emergency disconnect signal. Must use HTTPS and have an IPv4 or IPv6 address as the host.

<a href="#">Link to this property</a>

gateway\_proxy\_enabled: optional boolean

Enable gateway proxy filtering on TCP.

<a href="#">Link to this property</a>

gateway\_udp\_proxy\_enabled: optional boolean

Enable gateway proxy filtering on UDP.

<a href="#">Link to this property</a>

root\_certificate\_installation\_enabled: optional boolean

Enable installation of cloudflare managed root certificate.

<a href="#">Link to this property</a>

use\_zt\_virtual\_ip: optional boolean

Enable using CGNAT virtual IPv4.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.settings%20%3E%20(model)%20device_settings%20%3E%20(schema)>)

#### Zero TrustDevicesUnrevoke

##### [Unrevoke devices (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/unrevoke/methods/create)

Deprecated

POST/accounts/{account\_id}/devices/unrevoke

##### ModelsExpand Collapse

<details>

<summary>

UnrevokeCreateResponse = unknownor string

</summary>

One of the following:

unknown

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.unrevoke%20%3E%20(model)%20unrevoke_create_response%20%3E%20(schema)>)

#### Zero TrustDevicesOverride Codes

##### [Get override codes (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/override_codes/methods/list)

Deprecated

GET/accounts/{account\_id}/devices/{device\_id}/override\_codes

##### [Get override codes](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/override_codes/methods/get)

GET/accounts/{account\_id}/devices/registrations/{registration\_id}/override\_codes

##### ModelsExpand Collapse

<details>

<summary>

OverrideCodeListResponse object {disable\_for\_time }

</summary>

<details>

<summary>

disable\_for\_time: optional object {"1", "12", "24", 2 more }

</summary>

"1": optional string

Override code that is valid for 1 hour.

<a href="#">Link to this property</a>

"12": optional string

Override code that is valid for 12 hour2.

<a href="#">Link to this property</a>

"24": optional string

Override code that is valid for 24 hour.2.

<a href="#">Link to this property</a>

"3": optional string

Override code that is valid for 3 hours.

<a href="#">Link to this property</a>

"6": optional string

Override code that is valid for 6 hours.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(model)%20override_code_list_response%20%3E%20(schema)>)

<details>

<summary>

OverrideCodeGetResponse object {disable\_for\_time }

</summary>

disable\_for\_time: optional map\[string]

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(model)%20override_code_get_response%20%3E%20(schema)>)

#### Zero TrustIdentity Providers

##### [List Access identity providers](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/methods/list)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/identity\_providers

##### [Get an Access identity provider](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/identity\_providers/{identity\_provider\_id}

##### [Add an Access identity provider](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/identity\_providers

##### [Update an Access identity provider](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/methods/update)

PUT/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/identity\_providers/{identity\_provider\_id}

##### [Delete an Access identity provider](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/methods/delete)

DELETE/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/identity\_providers/{identity\_provider\_id}

##### ModelsExpand Collapse

<details>

<summary>

AzureAD object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 5 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

conditional\_access\_enabled: optional boolean

Should Cloudflare try to load authentication contexts from your account

<a href="#">Link to this property</a>

directory\_id: optional string

Your Azure directory uuid

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

<details>

<summary>

prompt: optional "login"or "select\_account"or "none"

Indicates the type of user interaction that is required. prompt=login forces the user to enter their credentials on that request, negating single-sign on. prompt=none is the opposite. It ensures that the user isn’t presented with any interactive prompt. If the request can’t be completed silently by using single-sign on, the Microsoft identity platform returns an interaction\_required error. prompt=select\_account interrupts single sign-on providing account selection experience listing all the accounts either in session or any remembered account or an option to choose to use a different account altogether.

</summary>

One of the following:

"login"

<a href="#">Link to this property</a>

"select\_account"

<a href="#">Link to this property</a>

"none"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_groups: optional boolean

Should Cloudflare try to load groups from your account

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20azure_ad%20%3E%20(schema)>)

<details>

<summary>

GenericOAuthConfig object {client\_id, client\_secret }

</summary>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)>)

<details>

<summary>

IdentityProvider = <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20azure_ad%20%3E%20(schema)">AzureAD</a> { config, name, type, 5 more } or object {config, name, type, 5 more } or object {config, name, type, 5 more } or 13 more

</summary>

One of the following:

<details>

<summary>

AzureAD object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 5 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

conditional\_access\_enabled: optional boolean

Should Cloudflare try to load authentication contexts from your account

<a href="#">Link to this property</a>

directory\_id: optional string

Your Azure directory uuid

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

<details>

<summary>

prompt: optional "login"or "select\_account"or "none"

Indicates the type of user interaction that is required. prompt=login forces the user to enter their credentials on that request, negating single-sign on. prompt=none is the opposite. It ensures that the user isn’t presented with any interactive prompt. If the request can’t be completed silently by using single-sign on, the Microsoft identity platform returns an interaction\_required error. prompt=select\_account interrupts single sign-on providing account selection experience listing all the accounts either in session or any remembered account or an option to choose to use a different account altogether.

</summary>

One of the following:

"login"

<a href="#">Link to this property</a>

"select\_account"

<a href="#">Link to this property</a>

"none"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_groups: optional boolean

Should Cloudflare try to load groups from your account

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCentrify object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {centrify\_account, centrify\_app\_id, claims, 3 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

centrify\_account: optional string

Your centrify account url

<a href="#">Link to this property</a>

centrify\_app\_id: optional string

Your centrify app id

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessFacebook object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGitHub object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGoogle object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, email\_claim\_name }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGoogleApps object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {apps\_domain, claims, client\_id, 4 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

apps\_domain: optional string

Your companies TLD

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

<details>

<summary>

prompt: optional "none"or "consent"or "select\_account"

Configures the prompt behavior for Google authentication.

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"consent"

<a href="#">Link to this property</a>

"select\_account"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

use\_login\_hint: optional boolean

Whether to use a previously authenticated Access email as a Google login hint when exactly one email matches the Workspace domain.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedin object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDC object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {auth\_url, certs\_url, claims, 6 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

auth\_url: optional string

The authorization\_endpoint URL of your IdP

<a href="#">Link to this property</a>

certs\_url: optional string

The jwks\_uri endpoint of your IdP to allow the IdP keys to sign the tokens

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

pkce\_enabled: optional boolean

Enable Proof Key for Code Exchange (PKCE)

<a href="#">Link to this property</a>

scopes: optional array of string

OAuth scopes

<a href="#">Link to this property</a>

token\_url: optional string

The token\_endpoint URL of your IdP

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOkta object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {authorization\_server\_id, claims, client\_id, 3 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

authorization\_server\_id: optional string

Your okta authorization server id

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

okta\_account: optional string

Your okta account url

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOnelogin object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 2 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

onelogin\_account: optional string

Your OneLogin account url

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessPingone object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 2 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

ping\_env\_id: optional string

Your PingOne environment identifier

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSAML object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {attributes, email\_attribute\_name, enable\_encryption, 7 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

attributes: optional array of string

A list of SAML attribute names that will be added to your signed JWT token and can be used in SAML policy rules.

<a href="#">Link to this property</a>

email\_attribute\_name: optional string

The attribute name for email in the SAML response.

<a href="#">Link to this property</a>

enable\_encryption: optional boolean

Enable SAML assertion encryption. When enabled, the Identity Provider will encrypt SAML assertions using the certificate from the assigned certificate set.

To enable encryption:

1. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>
2. Set this field to <code>true</code> and include <code>saml_certificate_set_id</code> in the PUT request
3. Configure the public certificate in your external Identity Provider

Note: Requires <code>saml_certificate_set_id</code> to be set when <code>true</code>.

<a href="#">Link to this property</a>

force\_authn: optional boolean

Asks the IdP to reauthenticate the user for each SAML authentication request.

<a href="#">Link to this property</a>

<details>

<summary>

header\_attributes: optional array of object {attribute\_name, header\_name }

Add a list of attribute names that will be returned in the response header from the Access callback.

</summary>

attribute\_name: optional string

attribute name from the IDP

<a href="#">Link to this property</a>

header\_name: optional string

header that will be added on the request to the origin

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

idp\_public\_certs: optional array of string

X509 certificate to verify the signature in the SAML authentication response

<a href="#">Link to this property</a>

issuer\_url: optional string

IdP Entity ID or Issuer URL

<a href="#">Link to this property</a>

max\_sso\_url\_length: optional number

The maximum URL length the IdP accepts for the SSO redirect URL. When the constructed SSO URL would exceed this length, the RelayState is stored server-side and a short nonce is passed to the IdP instead. Set this if your IdP enforces a URL length limit.

maximum100000

minimum512

<a href="#">Link to this property</a>

sign\_request: optional boolean

Sign the SAML authentication request with Access credentials. To verify the signature, use the public key from the Access certs endpoints.

<a href="#">Link to this property</a>

sso\_target\_url: optional string

URL to send the SAML authentication requests to

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessYandex object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOnetimepin object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {redirect\_url }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

redirect\_url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflare object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {redirect\_url, restrict\_to\_account\_members }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

redirect\_url: optional string

<a href="#">Link to this property</a>

restrict\_to\_account\_members: optional boolean

When enabled, only users who are members of your Cloudflare account can authenticate through this identity provider. When disabled, any user with a Cloudflare account can authenticate, subject to your Access policies.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessPasskeys object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {login\_page\_auto\_prompt, redirect\_url }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

login\_page\_auto\_prompt: optional boolean

When enabled, the Access login page automatically prompts the user to authenticate with a passkey.

<a href="#">Link to this property</a>

redirect\_url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider%20%3E%20(schema)>)

<details>

<summary>

IdentityProviderSCIMConfig object {enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

</summary>

enabled: optional boolean

A flag to enable or disable SCIM for the identity provider.

<a href="#">Link to this property</a>

<details>

<summary>

identity\_update\_behavior: optional "automatic"or "reauth"or "no\_action"

Indicates how a SCIM event updates a user identity used for policy evaluation. Use “automatic” to automatically update a user’s identity and augment it with fields from the SCIM user resource. Use “reauth” to force re-authentication on group membership updates, user identity update will only occur after successful re-authentication. With “reauth” identities will not contain fields from the SCIM user resource. With “no\_action” identities will not be changed by SCIM updates in any way and users will not be prompted to reauthenticate.

</summary>

One of the following:

"automatic"

<a href="#">Link to this property</a>

"reauth"

<a href="#">Link to this property</a>

"no\_action"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

scim\_base\_url: optional string

The base URL of Cloudflare’s SCIM V2.0 API endpoint.

<a href="#">Link to this property</a>

seat\_deprovision: optional boolean

A flag to remove a user’s seat in Zero Trust when they have been deprovisioned in the Identity Provider. This cannot be enabled unless user\_deprovision is also enabled.

<a href="#">Link to this property</a>

secret: optional string

A read-only token generated when the SCIM integration is enabled for the first time. It is redacted on subsequent requests. If you lose this you will need to refresh it at /access/identity\_providers/:idpID/refresh\_scim\_secret.

<a href="#">Link to this property</a>

user\_deprovision: optional boolean

A flag to enable revoking a user’s session in Access and Gateway when they have been deprovisioned in the Identity Provider.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)>)

<details>

<summary>

IdentityProviderType = "onetimepin"or "azureAD"or "saml"or 13 more

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

One of the following:

"onetimepin"

<a href="#">Link to this property</a>

"azureAD"

<a href="#">Link to this property</a>

"saml"

<a href="#">Link to this property</a>

"centrify"

<a href="#">Link to this property</a>

"facebook"

<a href="#">Link to this property</a>

"github"

<a href="#">Link to this property</a>

"google-apps"

<a href="#">Link to this property</a>

"google"

<a href="#">Link to this property</a>

"linkedin"

<a href="#">Link to this property</a>

"oidc"

<a href="#">Link to this property</a>

"okta"

<a href="#">Link to this property</a>

"onelogin"

<a href="#">Link to this property</a>

"pingone"

<a href="#">Link to this property</a>

"yandex"

<a href="#">Link to this property</a>

"cloudflare"

<a href="#">Link to this property</a>

"passkeys"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)>)

<details>

<summary>

IdentityProviderListResponse = <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20azure_ad%20%3E%20(schema)">AzureAD</a> { config, name, type, 5 more } or object {config, name, type, 5 more } or object {config, name, type, 5 more } or 13 more

</summary>

One of the following:

<details>

<summary>

AzureAD object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 5 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

conditional\_access\_enabled: optional boolean

Should Cloudflare try to load authentication contexts from your account

<a href="#">Link to this property</a>

directory\_id: optional string

Your Azure directory uuid

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

<details>

<summary>

prompt: optional "login"or "select\_account"or "none"

Indicates the type of user interaction that is required. prompt=login forces the user to enter their credentials on that request, negating single-sign on. prompt=none is the opposite. It ensures that the user isn’t presented with any interactive prompt. If the request can’t be completed silently by using single-sign on, the Microsoft identity platform returns an interaction\_required error. prompt=select\_account interrupts single sign-on providing account selection experience listing all the accounts either in session or any remembered account or an option to choose to use a different account altogether.

</summary>

One of the following:

"login"

<a href="#">Link to this property</a>

"select\_account"

<a href="#">Link to this property</a>

"none"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

support\_groups: optional boolean

Should Cloudflare try to load groups from your account

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCentrify object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {centrify\_account, centrify\_app\_id, claims, 3 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

centrify\_account: optional string

Your centrify account url

<a href="#">Link to this property</a>

centrify\_app\_id: optional string

Your centrify app id

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessFacebook object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGitHub object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGoogle object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, email\_claim\_name }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessGoogleApps object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {apps\_domain, claims, client\_id, 4 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

apps\_domain: optional string

Your companies TLD

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

<details>

<summary>

prompt: optional "none"or "consent"or "select\_account"

Configures the prompt behavior for Google authentication.

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"consent"

<a href="#">Link to this property</a>

"select\_account"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

use\_login\_hint: optional boolean

Whether to use a previously authenticated Access email as a Google login hint when exactly one email matches the Workspace domain.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedin object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDC object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {auth\_url, certs\_url, claims, 6 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

auth\_url: optional string

The authorization\_endpoint URL of your IdP

<a href="#">Link to this property</a>

certs\_url: optional string

The jwks\_uri endpoint of your IdP to allow the IdP keys to sign the tokens

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

pkce\_enabled: optional boolean

Enable Proof Key for Code Exchange (PKCE)

<a href="#">Link to this property</a>

scopes: optional array of string

OAuth scopes

<a href="#">Link to this property</a>

token\_url: optional string

The token\_endpoint URL of your IdP

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOkta object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {authorization\_server\_id, claims, client\_id, 3 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

authorization\_server\_id: optional string

Your okta authorization server id

<a href="#">Link to this property</a>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

okta\_account: optional string

Your okta account url

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOnelogin object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 2 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

onelogin\_account: optional string

Your OneLogin account url

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessPingone object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {claims, client\_id, client\_secret, 2 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

claims: optional array of string

Custom claims

<a href="#">Link to this property</a>

client\_id: optional string

Your OAuth Client ID

<a href="#">Link to this property</a>

client\_secret: optional string

Your OAuth Client Secret

<a href="#">Link to this property</a>

email\_claim\_name: optional string

The claim name for email in the id\_token response.

<a href="#">Link to this property</a>

ping\_env\_id: optional string

Your PingOne environment identifier

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSAML object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {attributes, email\_attribute\_name, enable\_encryption, 7 more }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

attributes: optional array of string

A list of SAML attribute names that will be added to your signed JWT token and can be used in SAML policy rules.

<a href="#">Link to this property</a>

email\_attribute\_name: optional string

The attribute name for email in the SAML response.

<a href="#">Link to this property</a>

enable\_encryption: optional boolean

Enable SAML assertion encryption. When enabled, the Identity Provider will encrypt SAML assertions using the certificate from the assigned certificate set.

To enable encryption:

1. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>
2. Set this field to <code>true</code> and include <code>saml_certificate_set_id</code> in the PUT request
3. Configure the public certificate in your external Identity Provider

Note: Requires <code>saml_certificate_set_id</code> to be set when <code>true</code>.

<a href="#">Link to this property</a>

force\_authn: optional boolean

Asks the IdP to reauthenticate the user for each SAML authentication request.

<a href="#">Link to this property</a>

<details>

<summary>

header\_attributes: optional array of object {attribute\_name, header\_name }

Add a list of attribute names that will be returned in the response header from the Access callback.

</summary>

attribute\_name: optional string

attribute name from the IDP

<a href="#">Link to this property</a>

header\_name: optional string

header that will be added on the request to the origin

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

idp\_public\_certs: optional array of string

X509 certificate to verify the signature in the SAML authentication response

<a href="#">Link to this property</a>

issuer\_url: optional string

IdP Entity ID or Issuer URL

<a href="#">Link to this property</a>

max\_sso\_url\_length: optional number

The maximum URL length the IdP accepts for the SSO redirect URL. When the constructed SSO URL would exceed this length, the RelayState is stored server-side and a short nonce is passed to the IdP instead. Set this if your IdP enforces a URL length limit.

maximum100000

minimum512

<a href="#">Link to this property</a>

sign\_request: optional boolean

Sign the SAML authentication request with Access credentials. To verify the signature, use the public key from the Access certs endpoints.

<a href="#">Link to this property</a>

sso\_target\_url: optional string

URL to send the SAML authentication requests to

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessYandex object {config, name, type, 5 more }

</summary>

config: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20generic_oauth_config%20%3E%20(schema)">GenericOAuthConfig</a> { client\_id, client\_secret }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOnetimepin object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {redirect\_url }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

redirect\_url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflare object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {redirect\_url, restrict\_to\_account\_members }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

redirect\_url: optional string

<a href="#">Link to this property</a>

restrict\_to\_account\_members: optional boolean

When enabled, only users who are members of your Cloudflare account can authenticate through this identity provider. When disabled, any user with a Cloudflare account can authenticate, subject to your Access policies.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessPasskeys object {config, name, type, 5 more }

</summary>

<details>

<summary>

config: object {login\_page\_auto\_prompt, redirect\_url }

The configuration parameters for the identity provider. To view the required parameters for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

</summary>

login\_page\_auto\_prompt: optional boolean

When enabled, the Access login page automatically prompts the user to authenticate with a passkey.

<a href="#">Link to this property</a>

redirect\_url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the identity provider, shown to users on the login page.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_type%20%3E%20(schema)">IdentityProviderType</a>

The type of identity provider. To determine the value for a specific provider, refer to our <a href="https://developers.cloudflare.com/cloudflare-one/identity/idp-integration/">developer documentation</a>.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

read\_only: optional boolean

Indicates that the identity provider is immutable and cannot be updated or deleted via the API.

<a href="#">Link to this property</a>

<details>

<summary>

saml\_certificate\_set: optional object {created\_at, uid, updated\_at, 2 more }

The SAML encryption certificate set details, including current and previous certificates. Only present for SAML identity providers with a certificate set assigned.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

saml\_certificate\_set\_id: optional string

The UID of the SAML encryption certificate set assigned to this Identity Provider. Only present for SAML identity providers with encryption configured. Create a certificate set via POST to <code>/identity_providers/{id}/saml_certificate</code>.

formatuuid

<a href="#">Link to this property</a>

scim\_config: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_scim_config%20%3E%20(schema)">IdentityProviderSCIMConfig</a> { enabled, identity\_update\_behavior, scim\_base\_url, 3 more }

The configuration settings for enabling a System for Cross-Domain Identity Management (SCIM) with the identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_list_response%20%3E%20(schema)>)

<details>

<summary>

IdentityProviderDeleteResponse object {id }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers%20%3E%20(model)%20identity_provider_delete_response%20%3E%20(schema)>)

#### Zero TrustIdentity ProvidersSCIM

#### Zero TrustIdentity ProvidersSCIMGroups

##### [List SCIM Group resources](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups/methods/list)

GET/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups

#### Zero TrustIdentity ProvidersSCIMUsers

##### [List SCIM User resources](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/users/methods/list)

GET/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/users

#### Zero TrustIdentity ProvidersSAML Certificate

##### [Create SAML encryption certificate for Identity Provider](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/saml_certificate/methods/create)

POST/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/saml\_certificate

##### ModelsExpand Collapse

<details>

<summary>

SAMLCertificateCreateResponse object {created\_at, uid, updated\_at, 2 more }

A SAML encryption certificate set containing current and optionally previous certificates for encryption key rotation.

</summary>

created\_at: string

Timestamp when the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp when the certificate set was last updated (e.g., during rotation)

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The currently active certificate used for encrypting SAML assertions

</summary>

is\_current: boolean

Indicates whether this is the currently active certificate

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date. Certificates are automatically rotated 30 days before expiration.

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

PEM-encoded X.509 certificate containing the public key. Configure this certificate in your external SAML Identity Provider to enable encryption.

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate, maintained during rotation to ensure continuity. Null if no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers.saml_certificate%20%3E%20(model)%20saml_certificate_create_response%20%3E%20(schema)>)

#### Zero TrustOrganizations

##### [Get your Zero Trust organization](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/methods/list)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/organizations

##### [Create your Zero Trust organization](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/organizations

##### [Update your Zero Trust organization](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/methods/update)

PUT/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/organizations

##### [Revoke all Access tokens for a user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/methods/revoke_users)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/organizations/revoke\_user

##### ModelsExpand Collapse

<details>

<summary>

LoginDesign object {background\_color, footer\_text, header\_text, 2 more }

</summary>

background\_color: optional string

The background color on your login page.

<a href="#">Link to this property</a>

footer\_text: optional string

The text at the bottom of your login page.

<a href="#">Link to this property</a>

header\_text: optional string

The text at the top of your login page.

<a href="#">Link to this property</a>

logo\_path: optional string

The URL of the logo on your login page.

<a href="#">Link to this property</a>

text\_color: optional string

The text color on your login page.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations%20%3E%20(model)%20login_design%20%3E%20(schema)>)

<details>

<summary>

Organization object {allow\_authenticate\_via\_warp, auth\_domain, auto\_redirect\_to\_identity, 16 more }

</summary>

allow\_authenticate\_via\_warp: optional boolean

When set to true, users can authenticate via WARP for any application in your organization. Application settings will take precedence over this value.

<a href="#">Link to this property</a>

auth\_domain: optional string

The unique subdomain assigned to your Zero Trust organization. If omitted on creation, a unique subdomain is auto-generated in the format <code>adjective-noun-hex4</code> (e.g. <code>frosty-moon-7a3b.cloudflareaccess.com</code>).

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login.

<a href="#">Link to this property</a>

<details>

<summary>

custom\_pages: optional object {forbidden, identity\_denied }

</summary>

forbidden: optional string

The uid of the custom page to use when a user is denied access after failing a non-identity rule.

<a href="#">Link to this property</a>

identity\_denied: optional string

The uid of the custom page to use when a user is denied access.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deny\_unmatched\_requests: optional boolean

Determines whether to deny all requests to Cloudflare-protected resources that lack an associated Access application. If enabled, you must explicitly configure an Access application and policy to allow traffic to your Cloudflare-protected resources. For domains you want to be public across all subdomains, add the domain to the <code>deny_unmatched_requests_exempted_zone_names</code> array.

<a href="#">Link to this property</a>

deny\_unmatched\_requests\_exempted\_zone\_names: optional array of string

Contains zone names to exempt from the <code>deny_unmatched_requests</code> feature. Requests to a subdomain in an exempted zone will block unauthenticated traffic by default if there is a configured Access application and policy that matches the request.

<a href="#">Link to this property</a>

is\_ui\_read\_only: optional boolean

Lock all settings as Read-Only in the Dashboard, regardless of user permission. Updates may only be made via the API or Terraform for this account when enabled.

<a href="#">Link to this property</a>

login\_design: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.organizations%20%3E%20(model)%20login_design%20%3E%20(schema)">LoginDesign</a> { background\_color, footer\_text, header\_text, 2 more }

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_config: optional object {allowed\_authenticators, amr\_matching\_session\_duration, required\_aaguids, session\_duration }

Configures multi-factor authentication (MFA) settings for an organization.

</summary>

<details>

<summary>

allowed\_authenticators: optional array of "totp"or "biometrics"or "security\_key"or 2 more

Lists the MFA methods that users can authenticate with. The <code>piv_key</code> and <code>ssh_fido2_key</code> values are supported only for infrastructure applications.

</summary>

One of the following:

"totp"

<a href="#">Link to this property</a>

"biometrics"

<a href="#">Link to this property</a>

"security\_key"

<a href="#">Link to this property</a>

"piv\_key"

<a href="#">Link to this property</a>

"ssh\_fido2\_key"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

amr\_matching\_session\_duration: optional string

Allows a user to skip MFA via Authentication Method Reference (AMR) matching when the AMR claim provided by the IdP the user used to authenticate contains “mfa”. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days).

<a href="#">Link to this property</a>

required\_aaguids: optional string

Specifies a Cloudflare List of required FIDO2 authenticator device AAGUIDs.

formatuuid

<a href="#">Link to this property</a>

session\_duration: optional string

Defines the duration of an MFA session. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days). Examples:<code>5m</code> or <code>24h</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_piv\_key\_requirements: optional object {pin\_policy, require\_fips\_device, ssh\_key\_size, 2 more }

Configures PIV key requirements for MFA using hardware security keys.

</summary>

<details>

<summary>

pin\_policy: optional "never"or "once"or "always"

Defines when a PIN is required to use the SSH key. Valid values: <code>never</code> (no PIN required), <code>once</code> (PIN required once per session), <code>always</code> (PIN required for each use).

</summary>

One of the following:

"never"

<a href="#">Link to this property</a>

"once"

<a href="#">Link to this property</a>

"always"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

require\_fips\_device: optional boolean

Requires the PIV key to be stored on a FIPS 140-2 Level 1 or higher validated device.

<a href="#">Link to this property</a>

<details>

<summary>

ssh\_key\_size: optional array of 256or 384or 521or 3 more

Specifies the allowed SSH key sizes in bits. Valid sizes depend on key type. Ed25519 has a fixed key size and does not accept this parameter.

</summary>

One of the following:

256

<a href="#">Link to this property</a>

384

<a href="#">Link to this property</a>

521

<a href="#">Link to this property</a>

2048

<a href="#">Link to this property</a>

3072

<a href="#">Link to this property</a>

4096

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ssh\_key\_type: optional array of "ecdsa"or "ed25519"or "rsa"

Specifies the allowed SSH key types. Valid values are <code>ecdsa</code>, <code>ed25519</code>, and <code>rsa</code>.

</summary>

One of the following:

"ecdsa"

<a href="#">Link to this property</a>

"ed25519"

<a href="#">Link to this property</a>

"rsa"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

touch\_policy: optional "never"or "always"or "cached"

Defines when physical touch is required to use the SSH key. Valid values: <code>never</code> (no touch required), <code>always</code> (touch required for each use), <code>cached</code> (touch cached for 15 seconds).

</summary>

One of the following:

"never"

<a href="#">Link to this property</a>

"always"

<a href="#">Link to this property</a>

"cached"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mfa\_required\_for\_all\_apps: optional boolean

Determines whether global MFA settings apply to applications by default. The organization must have MFA enabled with at least one authentication method and a session duration configured. Note: ‘allowed\_authenticators’ cannot contain only the infrastructure SSH authenticators (‘piv\_key’ and ‘ssh\_fido2\_key’) if the organization has any non-infrastructure applications.

<a href="#">Link to this property</a>

name: optional string

The name of your Zero Trust organization. When omitted on creation, defaults to the provided auth\_domain; when both are omitted, defaults to the auto-generated subdomain slug (e.g. frosty-moon-7a3b).

<a href="#">Link to this property</a>

<details>

<summary>

service\_token\_inactivity: optional object {action, enabled, inactivity\_threshold\_days }

Configures automatic enforcement for inactive service tokens. A service token is inactive if no policy references it, and it has not successfully authenticated with an Access application during the selected inactivity period. This setting applies to every service token in your Zero Trust account.

</summary>

<details>

<summary>

action: "disable"or "delete"

The action applied to an inactive service token.

</summary>

One of the following:

"disable"

<a href="#">Link to this property</a>

"delete"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: boolean

Whether automatic enforcement for inactive service tokens is enabled.

<a href="#">Link to this property</a>

inactivity\_threshold\_days: number

The number of days a service token must be inactive before the configured action is applied.

maximum365

minimum30

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for applications will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

strict\_service\_token\_auth: optional boolean

Enables new behaviors for requests made with Access service tokens. Unauthorized requests emit audit logs, and return a 401 or 403 status code in the response instead of redirecting to the login page. Successful requests no longer receive a CF\_Authorization cookie in the response. Zero Trust organizations created on or after October 5, 2026 will have this setting enabled by default, and cannot disable it.

<a href="#">Link to this property</a>

ui\_read\_only\_toggle\_reason: optional string

A description of the reason why the UI read only field is being toggled.

<a href="#">Link to this property</a>

user\_seat\_expiration\_inactive\_time: optional string

The amount of time a user seat is inactive before it expires. When the user seat exceeds the set time of inactivity, the user is removed as an active seat and no longer counts against your Teams seat count. Minimum value for this setting is 1 month (730h). Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: <code>ns</code>, <code>us</code> (or <code>µs</code>), <code>ms</code>, <code>s</code>, <code>m</code>, <code>h</code>.

<a href="#">Link to this property</a>

warp\_auth\_non\_browser\_401: optional boolean

When enabled, unsuccessful WARP authentication requests with a non-HTML Accept header return a 401 response instead of redirecting to the login page.

<a href="#">Link to this property</a>

warp\_auth\_session\_duration: optional string

The amount of time that tokens issued for applications will be valid. Must be in the format <code>30m</code> or <code>2h45m</code>. Valid time units are: m, h.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations%20%3E%20(model)%20organization%20%3E%20(schema)>)

<details>

<summary>

OrganizationListResponse object {allow\_authenticate\_via\_warp, auth\_domain, auto\_redirect\_to\_identity, 17 more }

</summary>

allow\_authenticate\_via\_warp: optional boolean

When set to true, users can authenticate via WARP for any application in your organization. Application settings will take precedence over this value.

<a href="#">Link to this property</a>

auth\_domain: optional string

The unique subdomain assigned to your Zero Trust organization. If omitted on creation, a unique subdomain is auto-generated in the format <code>adjective-noun-hex4</code> (e.g. <code>frosty-moon-7a3b.cloudflareaccess.com</code>).

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login.

<a href="#">Link to this property</a>

<details>

<summary>

custom\_pages: optional object {forbidden, identity\_denied }

</summary>

forbidden: optional string

The uid of the custom page to use when a user is denied access after failing a non-identity rule.

<a href="#">Link to this property</a>

identity\_denied: optional string

The uid of the custom page to use when a user is denied access.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deny\_unmatched\_requests: optional boolean

Determines whether to deny all requests to Cloudflare-protected resources that lack an associated Access application. If enabled, you must explicitly configure an Access application and policy to allow traffic to your Cloudflare-protected resources. For domains you want to be public across all subdomains, add the domain to the <code>deny_unmatched_requests_exempted_zone_names</code> array.

<a href="#">Link to this property</a>

deny\_unmatched\_requests\_exempted\_zone\_names: optional array of string

Contains zone names to exempt from the <code>deny_unmatched_requests</code> feature. Requests to a subdomain in an exempted zone will block unauthenticated traffic by default if there is a configured Access application and policy that matches the request.

<a href="#">Link to this property</a>

is\_ui\_read\_only: optional boolean

Lock all settings as Read-Only in the Dashboard, regardless of user permission. Updates may only be made via the API or Terraform for this account when enabled.

<a href="#">Link to this property</a>

login\_design: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.organizations%20%3E%20(model)%20login_design%20%3E%20(schema)">LoginDesign</a> { background\_color, footer\_text, header\_text, 2 more }

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_config: optional object {allowed\_authenticators, amr\_matching\_session\_duration, required\_aaguids, session\_duration }

Configures multi-factor authentication (MFA) settings for an organization.

</summary>

<details>

<summary>

allowed\_authenticators: optional array of "totp"or "biometrics"or "security\_key"or 2 more

Lists the MFA methods that users can authenticate with. The <code>piv_key</code> and <code>ssh_fido2_key</code> values are supported only for infrastructure applications.

</summary>

One of the following:

"totp"

<a href="#">Link to this property</a>

"biometrics"

<a href="#">Link to this property</a>

"security\_key"

<a href="#">Link to this property</a>

"piv\_key"

<a href="#">Link to this property</a>

"ssh\_fido2\_key"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

amr\_matching\_session\_duration: optional string

Allows a user to skip MFA via Authentication Method Reference (AMR) matching when the AMR claim provided by the IdP the user used to authenticate contains “mfa”. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days).

<a href="#">Link to this property</a>

required\_aaguids: optional string

Specifies a Cloudflare List of required FIDO2 authenticator device AAGUIDs.

formatuuid

<a href="#">Link to this property</a>

session\_duration: optional string

Defines the duration of an MFA session. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days). Examples:<code>5m</code> or <code>24h</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_piv\_key\_requirements: optional object {pin\_policy, require\_fips\_device, ssh\_key\_size, 2 more }

Configures PIV key requirements for MFA using hardware security keys.

</summary>

<details>

<summary>

pin\_policy: optional "never"or "once"or "always"

Defines when a PIN is required to use the SSH key. Valid values: <code>never</code> (no PIN required), <code>once</code> (PIN required once per session), <code>always</code> (PIN required for each use).

</summary>

One of the following:

"never"

<a href="#">Link to this property</a>

"once"

<a href="#">Link to this property</a>

"always"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

require\_fips\_device: optional boolean

Requires the PIV key to be stored on a FIPS 140-2 Level 1 or higher validated device.

<a href="#">Link to this property</a>

<details>

<summary>

ssh\_key\_size: optional array of 256or 384or 521or 3 more

Specifies the allowed SSH key sizes in bits. Valid sizes depend on key type. Ed25519 has a fixed key size and does not accept this parameter.

</summary>

One of the following:

256

<a href="#">Link to this property</a>

384

<a href="#">Link to this property</a>

521

<a href="#">Link to this property</a>

2048

<a href="#">Link to this property</a>

3072

<a href="#">Link to this property</a>

4096

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ssh\_key\_type: optional array of "ecdsa"or "ed25519"or "rsa"

Specifies the allowed SSH key types. Valid values are <code>ecdsa</code>, <code>ed25519</code>, and <code>rsa</code>.

</summary>

One of the following:

"ecdsa"

<a href="#">Link to this property</a>

"ed25519"

<a href="#">Link to this property</a>

"rsa"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

touch\_policy: optional "never"or "always"or "cached"

Defines when physical touch is required to use the SSH key. Valid values: <code>never</code> (no touch required), <code>always</code> (touch required for each use), <code>cached</code> (touch cached for 15 seconds).

</summary>

One of the following:

"never"

<a href="#">Link to this property</a>

"always"

<a href="#">Link to this property</a>

"cached"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mfa\_required\_for\_all\_apps: optional boolean

Determines whether global MFA settings apply to applications by default. The organization must have MFA enabled with at least one authentication method and a session duration configured. Note: ‘allowed\_authenticators’ cannot contain only the infrastructure SSH authenticators (‘piv\_key’ and ‘ssh\_fido2\_key’) if the organization has any non-infrastructure applications.

<a href="#">Link to this property</a>

name: optional string

The name of your Zero Trust organization. When omitted on creation, defaults to the provided auth\_domain; when both are omitted, defaults to the auto-generated subdomain slug (e.g. frosty-moon-7a3b).

<a href="#">Link to this property</a>

<details>

<summary>

service\_token\_inactivity: optional object {action, enabled, inactivity\_threshold\_days }

Configures automatic enforcement for inactive service tokens. A service token is inactive if no policy references it, and it has not successfully authenticated with an Access application during the selected inactivity period. This setting applies to every service token in your Zero Trust account.

</summary>

<details>

<summary>

action: "disable"or "delete"

The action applied to an inactive service token.

</summary>

One of the following:

"disable"

<a href="#">Link to this property</a>

"delete"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: boolean

Whether automatic enforcement for inactive service tokens is enabled.

<a href="#">Link to this property</a>

inactivity\_threshold\_days: number

The number of days a service token must be inactive before the configured action is applied.

maximum365

minimum30

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for applications will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

strict\_service\_token\_auth: optional boolean

Enables new behaviors for requests made with Access service tokens. Unauthorized requests emit audit logs, and return a 401 or 403 status code in the response instead of redirecting to the login page. Successful requests no longer receive a CF\_Authorization cookie in the response. Zero Trust organizations created on or after October 5, 2026 will have this setting enabled by default, and cannot disable it.

<a href="#">Link to this property</a>

trusted\_accounts: optional array of string

The account tags of organizations trusted by this organization for policy and device posture sharing.

<a href="#">Link to this property</a>

ui\_read\_only\_toggle\_reason: optional string

A description of the reason why the UI read only field is being toggled.

<a href="#">Link to this property</a>

user\_seat\_expiration\_inactive\_time: optional string

The amount of time a user seat is inactive before it expires. When the user seat exceeds the set time of inactivity, the user is removed as an active seat and no longer counts against your Teams seat count. Minimum value for this setting is 1 month (730h). Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: <code>ns</code>, <code>us</code> (or <code>µs</code>), <code>ms</code>, <code>s</code>, <code>m</code>, <code>h</code>.

<a href="#">Link to this property</a>

warp\_auth\_non\_browser\_401: optional boolean

When enabled, unsuccessful WARP authentication requests with a non-HTML Accept header return a 401 response instead of redirecting to the login page.

<a href="#">Link to this property</a>

warp\_auth\_session\_duration: optional string

The amount of time that tokens issued for applications will be valid. Must be in the format <code>30m</code> or <code>2h45m</code>. Valid time units are: m, h.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations%20%3E%20(model)%20organization_list_response%20%3E%20(schema)>)

<details>

<summary>

OrganizationRevokeUsersResponse = trueor false

</summary>

One of the following:

true

<a href="#">Link to this property</a>

false

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations%20%3E%20(model)%20organization_revoke_users_response%20%3E%20(schema)>)

#### Zero TrustOrganizationsDOH

##### [Get your Zero Trust organization DoH settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/doh/methods/get)

GET/accounts/{account\_id}/access/organizations/doh

##### [Update your Zero Trust organization DoH settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/doh/methods/update)

PUT/accounts/{account\_id}/access/organizations/doh

##### ModelsExpand Collapse

<details>

<summary>

DOHGetResponse object {id, client\_id, doh\_jwt\_duration, 4 more }

</summary>

id: optional string

The ID of the service token.

maxLength36

<a href="#">Link to this property</a>

client\_id: optional string

The Client ID for the service token. Access will check for this value in the <code>CF-Access-Client-ID</code> request header.

<a href="#">Link to this property</a>

doh\_jwt\_duration: optional string

The duration the DoH JWT is valid for. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h. Note that the maximum duration for this setting is the same as the key rotation period on the account.

<a href="#">Link to this property</a>

duration: optional string

The duration for how long the service token will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>, or the special value <code>forever</code> for non-expiring tokens. Valid time units are: ns, us (or µs), ms, s, m, h. The default is 1 year in hours (8760h).

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the service token is enabled. A disabled service token cannot be used to authenticate; both its current and previous <code>client_secret</code> stop being accepted, but the token itself is preserved and can be re-enabled at any time. Defaults to enabled when omitted on create.

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

The name of the service token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.doh%20%3E%20(model)%20doh_get_response%20%3E%20(schema)>)

<details>

<summary>

DOHUpdateResponse object {id, client\_id, doh\_jwt\_duration, 4 more }

</summary>

id: optional string

The ID of the service token.

maxLength36

<a href="#">Link to this property</a>

client\_id: optional string

The Client ID for the service token. Access will check for this value in the <code>CF-Access-Client-ID</code> request header.

<a href="#">Link to this property</a>

doh\_jwt\_duration: optional string

The duration the DoH JWT is valid for. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h. Note that the maximum duration for this setting is the same as the key rotation period on the account. Default expiration is 24h

<a href="#">Link to this property</a>

duration: optional string

The duration for how long the service token will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>, or the special value <code>forever</code> for non-expiring tokens. Valid time units are: ns, us (or µs), ms, s, m, h. The default is 1 year in hours (8760h).

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the service token is enabled. A disabled service token cannot be used to authenticate; both its current and previous <code>client_secret</code> stop being accepted, but the token itself is preserved and can be re-enabled at any time. Defaults to enabled when omitted on create.

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

The name of the service token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.doh%20%3E%20(model)%20doh_update_response%20%3E%20(schema)>)

#### Zero TrustSeats

##### [Update a user seat](https://developers.cloudflare.com/api/resources/zero_trust/subresources/seats/methods/edit)

PATCH/accounts/{account\_id}/access/seats

##### ModelsExpand Collapse

<details>

<summary>

Seat object {access\_seat, created\_at, gateway\_seat, 2 more }

</summary>

access\_seat: optional boolean

True if the seat is part of Access.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

gateway\_seat: optional boolean

True if the seat is part of Gateway.

<a href="#">Link to this property</a>

seat\_uid: optional string

The unique API identifier for the Zero Trust seat.

maxLength36

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.seats%20%3E%20(model)%20seat%20%3E%20(schema)>)

#### Zero TrustAccess

#### Zero TrustAccessAI Controls

#### Zero TrustAccessAI ControlsMcp

#### Zero TrustAccessAI ControlsMcpPortals

##### [List MCP Portals](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/list)

GET/accounts/{account\_id}/access/ai-controls/mcp/portals

##### [Create a new MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/create)

POST/accounts/{account\_id}/access/ai-controls/mcp/portals

##### [Read details of an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/read)

GET/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### [Update an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/update)

PUT/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### [Delete an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/delete)

DELETE/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### ModelsExpand Collapse

<details>

<summary>

PortalListResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_list_response%20%3E%20(schema)>)

<details>

<summary>

PortalCreateResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_create_response%20%3E%20(schema)>)

<details>

<summary>

PortalReadResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_read_response%20%3E%20(schema)>)

<details>

<summary>

PortalUpdateResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_update_response%20%3E%20(schema)>)

<details>

<summary>

PortalDeleteResponse object {id, hostname, name, 8 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

</summary>

</details>

</details>

<!-- Cloudflare Markdown for Agents: incomplete conversion; source HTML truncated at the conversion size limit -->
