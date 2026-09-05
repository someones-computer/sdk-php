# # PortAllocation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**swarm** | **string** | The cluster this port is claimed on. Deleting the cluster takes its allocations with it — a reservation on a swarm that no longer exists is not holding anything back. | [optional]
**application** | **string** |  | [optional]
**deployment_name** | **string** | The deployment name this reservation belongs to — {@see Deployment::$name}, or &#x60;&#39;&#39;&#x60; for a revision that carries no name (before the field existed, or a client that never sent one), which is its own stable scope rather than a wildcard: every unnamed revision of an application shares it, exactly the single continuous scope every application had before this column existed. | [optional]
**service_name** | **string** | The compose service name, as the customer&#39;s file spells it. | [optional]
**target_port** | **int** | The container port traffic is forwarded to. | [optional]
**protocol** | **string** |  | [optional]
**published_port** | **int** | What the world connects to. Unique per protocol on this cluster. | [optional]
**assigned** | **bool** | Whether the platform chose this number or the compose file did. | [optional]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
