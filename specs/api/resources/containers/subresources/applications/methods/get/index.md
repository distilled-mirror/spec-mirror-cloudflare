---
title: Get a single application by id
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Containers](https://developers.cloudflare.com/api/resources/containers)

[Applications](https://developers.cloudflare.com/api/resources/containers/subresources/applications)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a single application by id

GET/accounts/{account\_id}/containers/applications/{application\_id}

Returns a single application by id.

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

`Workers Containers Write``Workers Containers Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

application\_id: string

An Application ID represents an identifier of an application.

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20application_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

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

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

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

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, account\_id, configuration, 13 more } or object {id, account\_id, created\_at, 7 more }

The public Containers API returns an application.

</summary>

One of the following:

<details>

<summary>

CcScheduledApplication object {id, account\_id, configuration, 13 more }

Describes an application and the parameters that govern how it places its instances.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: object {image, authorized\_keys, command, 4 more }

User-specified container configuration.

</summary>

image: string

Image url.

<a href="#">Link to this property</a>

<details>

<summary>

authorized\_keys: optional array of object {public\_key, name }

</summary>

public\_key: string

An SSH public key.

<a href="#">Link to this property</a>

name: optional string

Optional human readable name for this key.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

command: optional array of string

The command that runs when the container starts, passed to the entrypoint. You can override this at run-time. If you override only the command, it gets passed to the default entrypoint specified in the image.

<a href="#">Link to this property</a>

entrypoint: optional array of string

The entry point for the container, specifying the executable to run when the container starts. You can override this at run-time. If you do, the default command from the image is ignored. Specify both entrypoint and command at run-time to completely replace the image defaults.

<a href="#">Link to this property</a>

<details>

<summary>

environment\_variables: optional array of object {name, value }

Container environment variables.

</summary>

name: string

An environment variable name.

<a href="#">Link to this property</a>

value: string

An environment variable value.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instance\_type: optional "lite"or "basic"or "standard-1"or 3 more

The instance type configures vCPU, memory, and disk.

- “lite”: 1/16 vCPU, 256 MiB memory, 2 GB disk
- “basic”: 1/4 vCPU, 1 GiB memory, 4 GB disk
- “standard-1”: 1/2 vCPU, 4 GiB memory, 8 GB disk
- “standard-2”: 1 vCPU, 6 GiB memory, 12 GB disk
- “standard-3”: 2 vCPU, 8 GiB memory, 16 GB disk
- “standard-4”: 4 vCPU, 12 GiB memory, 20 GB disk

</summary>

One of the following:

"lite"

<a href="#">Link to this property</a>

"basic"

<a href="#">Link to this property</a>

"standard-1"

<a href="#">Link to this property</a>

"standard-2"

<a href="#">Link to this property</a>

"standard-3"

<a href="#">Link to this property</a>

"standard-4"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Settings for deployment observability such as logging.

</summary>

<details>

<summary>

logs: optional object {enabled }

Observability logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

instances: number

Number of deployments to create.

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

<details>

<summary>

scheduling\_policy: "default"or "durable\_object"

The scheduling policy to use for an application.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"durable\_object"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

version: number

<a href="#">Link to this property</a>

active\_rollout\_id: optional string

An identifier for a specific rollout within an application.

<a href="#">Link to this property</a>

<details>

<summary>

constraints: optional object {jurisdiction, regions }

</summary>

jurisdiction: optional string

Restricts placement to datacenters in the selected jurisdiction. Choose “eu”, “fedramp”, or “us”. When combined with regions, EU supports EEUR and WEUR while FedRAMP and US support ENAM and WNAM.

<a href="#">Link to this property</a>

regions: optional array of string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: optional object {namespace\_id }

Durable object configuration stored on and returned from a Cloudchamber application.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {errors, instances, summary }

</summary>

<details>

<summary>

errors: array of object {event, instance\_id }

</summary>

<details>

<summary>

event: object {id, details, message, 4 more }

An event within a Placement or a Job.

</summary>

id: string

<a href="#">Link to this property</a>

details: map\[unknown]

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

name: "SchedulerPlaced"or "NetworkingIPAssigned"or "VMStarted"or 14 more

Name of the event that describes the kind event that happened.

- SchedulerPlaced: It’s the first event that creates a container placement. It happens when the Containers runtime was able to retrieve deployment resources and start verifying everything is correct.
- NetworkingIPAssigned: It’s sent when the Containers runtime maps the IP to the container.
- VMStarted: It’s sent when the Containers runtime starts the VM. The container might remain unhealthy at this point.
- ImagePulled: It’s sent when the Containers runtime pulls the image successfully.
- ImagePullError: It’s sent when the Containers runtime is having issues pulling the image. The message and details have more information on what happened for debugging.
- VMFailedToStart: It’s sent when the Containers runtime was unable to boot the VM.
- VMStopping: It’s sent when the scheduler is stopping the VM.
- VMStopped: It’s sent when the VM finally exits.
- VMFailed: It’s sent when the scheduling of the VM failed in the current location.
- RuntimeStartFailed: It’s sent when the runtime hits an internal error.
- SSHStarted: It’s sent when the container gains network connectivity and opens the SSH port. Containers only send this event when SSH keys exist.
- CheckUpdate: Sent when the status of a health or readiness check changes. This may also affect the health status of the placement.
- DurableObjectConnected: Sent when a durable object instance connects and gains control of the deployment. This event is only sent for durable object deployments. It is sent after VMStarted.
- ContainerStarted: It’s sent when the container starts running.

</summary>

One of the following:

"SchedulerPlaced"

<a href="#">Link to this property</a>

"NetworkingIPAssigned"

<a href="#">Link to this property</a>

"VMStarted"

<a href="#">Link to this property</a>

"ImagePulled"

<a href="#">Link to this property</a>

"ImagePullError"

<a href="#">Link to this property</a>

"VMFailedToStart"

<a href="#">Link to this property</a>

"NetworkingIPAssignmentFailed"

<a href="#">Link to this property</a>

"VMRunning"

<a href="#">Link to this property</a>

"VMStopping"

<a href="#">Link to this property</a>

"VMStopped"

<a href="#">Link to this property</a>

"VMFailed"

<a href="#">Link to this property</a>

"RuntimeStartFailed"

<a href="#">Link to this property</a>

"SSHStarted"

<a href="#">Link to this property</a>

"ServiceHealthUpdates"

<a href="#">Link to this property</a>

"CheckUpdate"

<a href="#">Link to this property</a>

"DurableObjectConnected"

<a href="#">Link to this property</a>

"ContainerStarted"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusChange: map\[unknown]

<a href="#">Link to this property</a>

time: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

type: "Info"or "Error"or "Warn"or 2 more

</summary>

One of the following:

"Info"

<a href="#">Link to this property</a>

"Error"

<a href="#">Link to this property</a>

"Warn"

<a href="#">Link to this property</a>

"UserError"

<a href="#">Link to this property</a>

"SystemError"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

instance\_id: string

An instance ID represents an identifier of an instance configuration that maintains an underlying placement.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

instances: object {active, assigned }

Shows a count of application instance states.

</summary>

active: number

Number of instances whose runtime reports the container as running (container\_status = “running”). This is a subset of the placements that remain up: an instance that is already bound to a Durable Object and serving traffic is counted under “assigned” until its container\_status catches up to “running”, so container\_status can briefly lag Durable Object attachment under churn. To estimate running, Durable-Object-bound instances, sum “active” + “assigned” rather than reading “active” alone.

<a href="#">Link to this property</a>

assigned: number

Number of instances bound to a Durable Object with a running placement whose container\_status remains behind “running”. These count as live, serving instances; “active” + “assigned” approximates the running, Durable-Object-bound count.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

summary: optional "healthy"or "degraded"or "unhealthy"or "pending"

High-level health assessment. Only populated for “new\_instances” strategy. Based on a sample of target-version instances rather than a full count.

- “pending”: Zero target-version instances exist yet.
- “healthy”: Every sampled target-version instance reports running or active.
- “degraded”: Some sampled instances remain starting or scheduling.
- “unhealthy”: One or more sampled instances have failed.

</summary>

One of the following:

"healthy"

<a href="#">Link to this property</a>

"degraded"

<a href="#">Link to this property</a>

"unhealthy"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_instances: optional number

Maximum number of instances the application allows. This is relevant for applications that auto-scale.

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Top-level observability settings for the application. This field is mutually exclusive with configuration.observability.

</summary>

<details>

<summary>

logs: optional object {enabled }

Observability logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

rollout\_active\_grace\_period: optional number

Grace period for active instances to stay alive before becoming eligible for shutdown signal due to a rollout, in seconds. Defaults to 0.

maximum604800

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CcDurableObjectApplication object {id, account\_id, created\_at, 7 more }

Each Durable Object creates and manages the lifecycle of its container instance.

</summary>

id: string

An Application ID represents an identifier of an application.

<a href="#">Link to this property</a>

account\_id: string

A unique identifier for the user’s account.

<a href="#">Link to this property</a>

created\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

durable\_objects: object {namespace\_id }

Durable object configuration using a namespace ID.

</summary>

namespace\_id: string

The namespace ID of the durable object namespace to use for this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

The application name.

<a href="#">Link to this property</a>

scheduling\_policy: "durable\_object"

Selects a Durable Object-managed application. Each Durable Object creates and manages the lifecycle of its container instance. Configure application-wide observability settings here. Deployment configuration, scaling, placement constraints, versions, and rollouts do not apply.

<a href="#">Link to this property</a>

updated\_at: string

UTC timestamp string in ISO 8601 format.

<a href="#">Link to this property</a>

<details>

<summary>

configuration: optional object {authorized\_keys, wrangler\_ssh }

Application-wide settings for a Durable Object-managed application.

</summary>

<details>

<summary>

authorized\_keys: optional array of object {public\_key, name }

</summary>

public\_key: string

An SSH public key.

<a href="#">Link to this property</a>

name: optional string

Optional human readable name for this key.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

wrangler\_ssh: optional object {enabled, port }

Configuration properties for connecting with SSH to a container using Wrangler.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

port: optional number

maximum65535

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

health: optional object {instances, summary }

Aggregate current activity for the latest observed placement of each instance. Runtime snapshots feed periodic background sweeps. Counts refresh after each complete sweep. Instance listings retain their separate three-month history for failure discovery.

</summary>

<details>

<summary>

instances: object {active, starting }

Counts of observed non-terminal instances.

</summary>

active: number

Number of instances whose runtime reports running or stopping.

minimum0

<a href="#">Link to this property</a>

starting: number

Number of instances whose runtime reports starting.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summary: optional "pending"

Present as pending until the first activity sweep completes; omitted afterward.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

observability: optional object {logs }

Application-wide logging settings for a Durable Object-managed application. The application publishes these settings to its runtime metadata. Updating them does not create a deployment or rollout.

</summary>

<details>

<summary>

logs: optional object {enabled }

Application-wide logging settings.

</summary>

enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20containers.applications%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get a single application by id

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/containers/applications/$APPLICATION_ID \
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
    "id": "id",
    "account_id": "account_id",
    "configuration": {
      "image": "image",
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "created_at": "2021-04-01T12:32:41.488Z",
    "instances": 0,
    "name": "name",
    "scheduling_policy": "default",
    "updated_at": "2021-04-01T12:32:41.488Z",
    "version": 0,
    "active_rollout_id": "active_rollout_id",
    "constraints": {
      "jurisdiction": "jurisdiction",
      "regions": [
        "WNAM"
      ]
    },
    "durable_objects": {
      "namespace_id": "14758f1afd44c09b7992073ccf00b43d"
    },
    "health": {
      "errors": [
        {
          "event": {
            "id": "id",
            "details": {
              "foo": "bar"
            },
            "message": "message",
            "name": "SchedulerPlaced",
            "statusChange": {
              "foo": "bar"
            },
            "time": "2021-04-01T12:32:41.488Z",
            "type": "Info"
          },
          "instance_id": "instance_id"
        }
      ],
      "instances": {
        "active": 0,
        "assigned": 0
      },
      "summary": "healthy"
    },
    "max_instances": 0,
    "observability": {
      "logs": {
        "enabled": true
      }
    },
    "rollout_active_grace_period": 0
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
    "id": "id",
    "account_id": "account_id",
    "configuration": {
      "image": "image",
      "authorized_keys": [
        {
          "public_key": "public_key",
          "name": "name"
        }
      ],
      "command": [
        "myapp",
        "--default-option"
      ],
      "entrypoint": [
        "/bin/bash"
      ],
      "environment_variables": [
        {
          "name": "name",
          "value": "value"
        }
      ],
      "instance_type": "lite",
      "observability": {
        "logs": {
          "enabled": true
        }
      }
    },
    "created_at": "2021-04-01T12:32:41.488Z",
    "instances": 0,
    "name": "name",
    "scheduling_policy": "default",
    "updated_at": "2021-04-01T12:32:41.488Z",
    "version": 0,
    "active_rollout_id": "active_rollout_id",
    "constraints": {
      "jurisdiction": "jurisdiction",
      "regions": [
        "WNAM"
      ]
    },
    "durable_objects": {
      "namespace_id": "14758f1afd44c09b7992073ccf00b43d"
    },
    "health": {
      "errors": [
        {
          "event": {
            "id": "id",
            "details": {
              "foo": "bar"
            },
            "message": "message",
            "name": "SchedulerPlaced",
            "statusChange": {
              "foo": "bar"
            },
            "time": "2021-04-01T12:32:41.488Z",
            "type": "Info"
          },
          "instance_id": "instance_id"
        }
      ],
      "instances": {
        "active": 0,
        "assigned": 0
      },
      "summary": "healthy"
    },
    "max_instances": 0,
    "observability": {
      "logs": {
        "enabled": true
      }
    },
    "rollout_active_grace_period": 0
  },
  "success": true
}
```