---
title: Get Hyperdrive
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Hyperdrive](https://developers.cloudflare.com/api/resources/hyperdrive)

[Configs](https://developers.cloudflare.com/api/resources/hyperdrive/subresources/configs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get Hyperdrive

GET/accounts/{account\_id}/hyperdrive/configs/{hyperdrive\_id}

Returns the specified Hyperdrive configuration.

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

`Hyperdrive Write``Hyperdrive Read`

##### P ath ParametersExpand Collapse

account\_id: string

Define configurations using a unique string identifier.

maxLength32

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

hyperdrive\_id: string

Define configurations using a unique string identifier.

maxLength32

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20hyperdrive_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20response_info%20%3E%20(schema)">ResponseInfo</a> { code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, caching, name, 7 more }

</summary>

id: string

Define configurations using a unique string identifier.

maxLength32

<a href="#">Link to this property</a>

<details>

<summary>

caching: object {disabled, max\_age, stale\_while\_revalidate }

</summary>

disabled: boolean

Defines whether caching is disabled.

<a href="#">Link to this property</a>

max\_age: optional number

Defines the maximum duration (in seconds) items persist in the cache.

maximum3600

minimum1

<a href="#">Link to this property</a>

stale\_while\_revalidate: optional number

Defines the number of seconds the cache may serve a stale response.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The name of the Hyperdrive configuration. Used to identify the configuration in the Cloudflare dashboard and API.

maxLength2048

<a href="#">Link to this property</a>

<details>

<summary>

origin: object {database, host, password, 3 more } or object {access\_client\_id, access\_client\_secret, database, 4 more } or object {database, password, scheme, 2 more }

Combines database connection fields with exactly one supported network location.

</summary>

One of the following:

<details>

<summary>

PublicDatabase object {database, host, password, 3 more }

</summary>

database: string

Set the name of your origin database.

maxLength2048

<a href="#">Link to this property</a>

host: string

Defines the publicly reachable hostname or IP of your origin database. Private, loopback, and link-local IP addresses are not allowed.

<a href="#">Link to this property</a>

password: string

Set the password needed to access your origin database. The API never returns this write-only value.

maxLength2048

<a href="#">Link to this property</a>

port: number

Defines the port of your origin database. Defaults to 5432 for PostgreSQL or 3306 for MySQL if not specified.

maximum65535

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

scheme: "postgres"or "postgresql"or "mysql"

Specifies the URL scheme used to connect to your origin database.

</summary>

One of the following:

"postgres"

<a href="#">Link to this property</a>

"postgresql"

<a href="#">Link to this property</a>

"mysql"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user: string

Set the user of your origin database.

maxLength2048

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessProtectedDatabaseBehindCloudflareTunnel object {access\_client\_id, access\_client\_secret, database, 4 more }

</summary>

access\_client\_id: string

Defines the Client ID of the Access token to use when connecting to the origin database.

<a href="#">Link to this property</a>

access\_client\_secret: string

Defines the Client Secret of the Access Token to use when connecting to the origin database. The API never returns this write-only value.

<a href="#">Link to this property</a>

database: string

Set the name of your origin database.

maxLength2048

<a href="#">Link to this property</a>

host: string

Defines the host (hostname or IP) of your origin database.

<a href="#">Link to this property</a>

password: string

Set the password needed to access your origin database. The API never returns this write-only value.

maxLength2048

<a href="#">Link to this property</a>

<details>

<summary>

scheme: "postgres"or "postgresql"or "mysql"

Specifies the URL scheme used to connect to your origin database.

</summary>

One of the following:

"postgres"

<a href="#">Link to this property</a>

"postgresql"

<a href="#">Link to this property</a>

"mysql"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user: string

Set the user of your origin database.

maxLength2048

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DatabaseReachableThroughAWorkersVPC object {database, password, scheme, 2 more }

</summary>

database: string

Set the name of your origin database.

maxLength2048

<a href="#">Link to this property</a>

password: string

Set the password needed to access your origin database. The API never returns this write-only value.

maxLength2048

<a href="#">Link to this property</a>

<details>

<summary>

scheme: "postgres"or "postgresql"or "mysql"

Specifies the URL scheme used to connect to your origin database.

</summary>

One of the following:

"postgres"

<a href="#">Link to this property</a>

"postgresql"

<a href="#">Link to this property</a>

"mysql"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service\_id: string

The identifier of the Workers VPC Service to connect through. Hyperdrive will egress through the specified VPC Service to reach the origin database.

<a href="#">Link to this property</a>

user: string

Set the user of your origin database.

maxLength2048

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_on: optional string

Defines the creation time of the Hyperdrive configuration.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

integration: optional object {database\_branch\_name, database\_name, integration, 3 more }

Connects to a PlanetScale database using credentials managed by Cloudflare. The Cloudflare account must already be linked to PlanetScale in the Hyperdrive dashboard.

</summary>

database\_branch\_name: string

The name of the PlanetScale database branch.

maxLength2048

minLength1

<a href="#">Link to this property</a>

database\_name: string

The name of the PlanetScale database.

maxLength2048

minLength1

<a href="#">Link to this property</a>

integration: "planetscale"

The database integration used by this operation.

<a href="#">Link to this property</a>

organization\_name: string

The name of the PlanetScale organization.

maxLength2048

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

scheme: "postgres"or "postgresql"or "mysql"

Specifies the URL scheme used to connect to your origin database.

</summary>

One of the following:

"postgres"

<a href="#">Link to this property</a>

"postgresql"

<a href="#">Link to this property</a>

"mysql"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

custom\_database\_name: optional string

The database name to use when connecting. Defaults to <code>postgres</code> for PostgreSQL and <code>mysql</code> for MySQL.

maxLength2048

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_on: optional string

Defines the last modified time of the Hyperdrive configuration.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

mtls: optional object {ca\_certificate\_id, mtls\_certificate\_id, sslmode }

mTLS configuration for the origin connection. Cannot be used with VPC Service origins; TLS must be managed on the VPC Service.

</summary>

ca\_certificate\_id: optional string

Define CA certificate ID obtained after uploading CA cert.

<a href="#">Link to this property</a>

mtls\_certificate\_id: optional string

Define mTLS certificate ID obtained after uploading client cert.

<a href="#">Link to this property</a>

sslmode: optional string

PostgreSQL accepts <code>require</code>, <code>verify-ca</code>, and <code>verify-full</code>. MySQL accepts <code>REQUIRED</code>, <code>VERIFY_CA</code>, and <code>VERIFY_IDENTITY</code>. The verify modes require a CA certificate; the require modes cannot be used with a CA certificate.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

origin\_connection\_limit: optional number

The (soft) maximum number of connections the Hyperdrive is allowed to make to the origin database.

Maximum allowed: 20 for free tier accounts, 100 for paid tier accounts. If not specified, defaults to 20 for free tier and 60 for paid tier. Certain Cloudflare-managed origins may be permitted a higher limit. Contact Cloudflare if you need a higher limit.

minimum5

<a href="#">Link to this property</a>

restarted\_on: optional string

Defines the last time the Hyperdrive connection pool was explicitly restarted via the restart endpoint. Omitted if the pool has never been explicitly restarted.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Return the status of the API call success.

[Link to this property](#)%20hyperdrive.configs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get Hyperdrive

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/hyperdrive/configs/$HYPERDRIVE_ID \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "023e105f4ecef8ad9ca31a8372d0c353",
    "caching": {
      "disabled": true,
      "max_age": 1,
      "stale_while_revalidate": 0
    },
    "name": "example-hyperdrive",
    "origin": {
      "database": "postgres",
      "host": "database.example.com",
      "port": 5432,
      "scheme": "postgres",
      "user": "postgres"
    },
    "created_on": "2017-01-01T00:00:00Z",
    "integration": {
      "database_branch_name": "x",
      "database_name": "x",
      "integration": "planetscale",
      "organization_name": "x",
      "scheme": "postgres",
      "custom_database_name": "custom_database_name"
    },
    "modified_on": "2017-01-01T00:00:00Z",
    "mtls": {
      "ca_certificate_id": "00000000-0000-0000-0000-0000000000",
      "mtls_certificate_id": "00000000-0000-0000-0000-0000000000",
      "sslmode": "verify-full"
    },
    "origin_connection_limit": 60,
    "restarted_on": "2017-01-01T00:00:00Z"
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
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "023e105f4ecef8ad9ca31a8372d0c353",
    "caching": {
      "disabled": true,
      "max_age": 1,
      "stale_while_revalidate": 0
    },
    "name": "example-hyperdrive",
    "origin": {
      "database": "postgres",
      "host": "database.example.com",
      "port": 5432,
      "scheme": "postgres",
      "user": "postgres"
    },
    "created_on": "2017-01-01T00:00:00Z",
    "integration": {
      "database_branch_name": "x",
      "database_name": "x",
      "integration": "planetscale",
      "organization_name": "x",
      "scheme": "postgres",
      "custom_database_name": "custom_database_name"
    },
    "modified_on": "2017-01-01T00:00:00Z",
    "mtls": {
      "ca_certificate_id": "00000000-0000-0000-0000-0000000000",
      "mtls_certificate_id": "00000000-0000-0000-0000-0000000000",
      "sslmode": "verify-full"
    },
    "origin_connection_limit": 60,
    "restarted_on": "2017-01-01T00:00:00Z"
  },
  "success": true
}
```