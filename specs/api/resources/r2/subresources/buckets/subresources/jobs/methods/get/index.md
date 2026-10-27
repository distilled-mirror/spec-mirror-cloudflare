---
title: Get Bucket Job
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[R2](https://developers.cloudflare.com/api/resources/r2)

[Buckets](https://developers.cloudflare.com/api/resources/r2/subresources/buckets)

[Jobs](https://developers.cloudflare.com/api/resources/r2/subresources/buckets/subresources/jobs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get Bucket Job

GET/accounts/{account\_id}/r2/buckets/{bucket\_name}/jobs/{job\_id}

Gets the current status of a background job of any type for an R2 bucket. Poll this endpoint with the job identifier returned by Create Bucket Job until the status is `COMPLETED`, `FAILED`, or `CANCELLED`.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### P ath ParametersExpand Collapse

account\_id: string

Cloudflare account ID that owns the R2 resource.

maxLength32

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

bucket\_name: string

Name of the bucket.

maxLength64

minLength3

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20bucket_name%20%3E%20(schema)>)

job\_id: string

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20job_id%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

<details>

<summary>

"cf-r2-jurisdiction": optional "default"or "eu"or "us"or 2 more

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"eu"

<a href="#">Link to this property</a>

"us"

<a href="#">Link to this property</a>

"fedramp"

<a href="#">Link to this property</a>

"fedramp-high"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20cf-r2-jurisdiction%20%3E%20(schema)>)

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

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

messages: array of string

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, jobType, prefixDelete, 3 more } or object {id, jobType, startTime, 3 more }

Descriptor of a bucket background job, discriminated by <code>jobType</code>. Returned by the Create Bucket Job, Get Bucket Job and List Bucket Jobs endpoints. A small operation can already be <code>COMPLETED</code> when it is returned.

</summary>

One of the following:

<details>

<summary>

PrefixDelete object {id, jobType, prefixDelete, 3 more }

Descriptor of a prefix-delete job. An empty prefix indicates a job that empties the whole bucket.

</summary>

id: string

Unique identifier used to poll the job.

<a href="#">Link to this property</a>

jobType: "prefixDelete"

The job kind.

<a href="#">Link to this property</a>

<details>

<summary>

prefixDelete: object {deletedObjects, prefix, isBucketClear }

Details specific to the prefix-delete job.

</summary>

deletedObjects: number

Number of objects deleted by the job so far.

<a href="#">Link to this property</a>

prefix: string

The prefix matched against object keys. An empty string means the entire bucket.

<a href="#">Link to this property</a>

isBucketClear: optional boolean

True when the job was created to clear the entire bucket. This field can be absent on jobs created before Empty Bucket job tracking was introduced.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

startTime: string

When the job was created.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "ENQUEUED"or "RUNNING"or "COMPLETED"or 2 more

Lifecycle status of a bucket background job.

</summary>

One of the following:

"ENQUEUED"

<a href="#">Link to this property</a>

"RUNNING"

<a href="#">Link to this property</a>

"COMPLETED"

<a href="#">Link to this property</a>

"FAILED"

<a href="#">Link to this property</a>

"CANCELLED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

endTime: optional string

When the job finished. Absent while the job is still <code>ENQUEUED</code> or <code>RUNNING</code>.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

StorageClassMigration object {id, jobType, startTime, 3 more }

Descriptor of a bucket-wide storage-class migration job.

</summary>

id: string

Unique identifier used to poll the job.

<a href="#">Link to this property</a>

jobType: "storageClassMigration"

The job kind.

<a href="#">Link to this property</a>

startTime: string

When the job was created.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "ENQUEUED"or "RUNNING"or "COMPLETED"or 2 more

Lifecycle status of a bucket background job.

</summary>

One of the following:

"ENQUEUED"

<a href="#">Link to this property</a>

"RUNNING"

<a href="#">Link to this property</a>

"COMPLETED"

<a href="#">Link to this property</a>

"FAILED"

<a href="#">Link to this property</a>

"CANCELLED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storageClassMigration: object {destinationStorageClass, migratedObjects, sourceStorageClass, 6 more }

</summary>

<details>

<summary>

destinationStorageClass: "Standard"or "InfrequentAccess"

The storage class objects are migrated to. The source and destination storage classes always differ.

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

migratedObjects: number

Number of object versions migrated successfully.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

sourceStorageClass: "Standard"or "InfrequentAccess"

The storage class objects are migrated from.

</summary>

One of the following:

"Standard"

<a href="#">Link to this property</a>

"InfrequentAccess"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

failedBytes: optional number

Payload bytes belonging to failed object versions.

minimum0

<a href="#">Link to this property</a>

failedObjects: optional number

Number of object versions that failed migration.

minimum0

<a href="#">Link to this property</a>

migratedBytes: optional number

Object payload bytes migrated successfully. Present for Metadata Worker jobs.

minimum0

<a href="#">Link to this property</a>

migratedMetadataBytes: optional number

Object metadata bytes migrated successfully. Present for Metadata Worker jobs.

minimum0

<a href="#">Link to this property</a>

skippedBytes: optional number

Payload bytes belonging to skipped object versions.

minimum0

<a href="#">Link to this property</a>

skippedObjects: optional number

Number of object versions skipped.

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

endTime: optional string

When the job finished. Absent while the job is still <code>ENQUEUED</code> or <code>RUNNING</code>.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20r2.buckets.jobs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get Bucket Job

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/r2/buckets/$BUCKET_NAME/jobs/$JOB_ID \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "endTime": "2026-07-20T12:14:31Z",
    "id": "7f24658b-31d7-4b91-9a12-cb5a2c99b294",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 2481,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "COMPLETED"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "endTime": "2026-07-20T12:14:31Z",
    "id": "7f24658b-31d7-4b91-9a12-cb5a2c99b294",
    "jobType": "prefixDelete",
    "prefixDelete": {
      "deletedObjects": 2481,
      "isBucketClear": true,
      "prefix": ""
    },
    "startTime": "2026-07-20T12:00:00Z",
    "status": "COMPLETED"
  },
  "success": true
}
```