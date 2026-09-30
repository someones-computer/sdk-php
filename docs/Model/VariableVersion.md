# # VariableVersion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**variable** | [**\SomeonesComputer\Sdk\Model\Variable**](Variable.md) |  | [optional]
**version** | **int** |  | [optional]
**algo** | **string** | Encryption algorithm identifier, e.g. \&quot;xsalsa20poly1305\&quot;. Sensitive only. | [optional] [readonly]
**key_id** | **string** | Identifier of the key-encryption-key that wrapped this value. Sensitive only. | [optional] [readonly]
**nonce** | **string** |  | [optional] [readonly]
**ciphertext** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**created_by** | [**\SomeonesComputer\Sdk\Model\User**](User.md) |  | [optional]
**id** | **string** |  | [optional] [readonly]
**encrypted** | **string** | Populate an encrypted (sensitive) value. | [optional]
**plaintext** | **string** | Populate a plaintext (non-sensitive) value. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
