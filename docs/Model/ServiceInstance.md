# # ServiceInstance

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Operator-facing handle, unique across the estate: &#x60;pg17-1&#x60;, &#x60;mysql80-1&#x60;. | [optional]
**kind** | **string** |  | [optional]
**major_version** | **string** | The major version this engine *is*, as the catalogue names it: &#x60;17&#x60;, &#x60;16&#x60;, &#x60;11.8&#x60;, &#x60;8.4&#x60;, &#x60;8.0&#x60;. | [optional]
**image_ref** | **string** | The exact image this instance runs, pinned — never a floating upstream tag. | [optional]
**swarm** | **string** | Repoint the instance at a different context. | [optional]
**overlay_network** | **string** | The internal overlay this engine and every sidecar bound to it share. | [optional]
**state** | **string** | Moving to any state other than {@see ServiceInstanceState::Failed} clears a stale failure. | [optional] [default to 'requested']
**failure_reason** | **string** | Why the instance failed, carried beside the state as &#x60;Machine::$failure&#x60; already does. | [optional] [readonly]
**capacity_bytes** | [**\SomeonesComputer\Sdk\Model\ServiceInstanceCapacityBytes**](ServiceInstanceCapacityBytes.md) |  | [optional]
**observed_usage_bytes** | [**\SomeonesComputer\Sdk\Model\ServiceInstanceObservedUsageBytes**](ServiceInstanceObservedUsageBytes.md) |  | [optional]
**observed_at** | **\DateTime** |  | [optional] [readonly]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**catalogue_entry** | **string** | &#x60;postgres 17&#x60;, &#x60;mysql 8.0&#x60; — the catalogue entry this instance serves. | [optional] [readonly]
**serving** | **bool** |  | [optional] [readonly]
**admin_credential** | [**\SomeonesComputer\Sdk\Model\SealedSecret**](SealedSecret.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
