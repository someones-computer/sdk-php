# # RecoveryCode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | [**\SomeonesComputer\Sdk\Model\User**](User.md) |  | [optional]
**code_hash** | **string** | SHA-256 hex digest of the plaintext code; the only copy that is ever stored. | [optional]
**used_at** | **\DateTime** | When this code was spent; null means it is still usable. | [optional] [readonly]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**used** | **bool** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
