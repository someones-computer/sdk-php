# # ServiceBinding

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **string** |  | [optional]
**service** | **string** |  | [optional]
**injected_keys** | **string[]** | The environment variable names this binding contributes — one &#x60;DATABASE_URL&#x60; for a database, the four &#x60;S3_*&#x60; names for a bucket. | [optional]
**sidecar_service_name** | **string** | What the sidecar is called inside the tenant&#39;s stack — &#x60;db&#x60; unless something else claimed the name first. | [optional] [default to 'db']
**adopted_compose_service** | **string** | The compose service this binding replaced, or null for a binding somebody asked for directly. | [optional]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**adopted** | **bool** |  | [optional] [readonly]
**sidecar_credential** | [**\SomeonesComputer\Sdk\Model\SealedSecret**](SealedSecret.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
