# GameServerGameServerInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **string** |  |
**slug** | **string** |  | [default to '']
**name** | **string** |  | [default to '']
**kind** | **string** |  |
**version** | **string** | Null takes the game&#39;s default version. | [optional]
**settings** | **array<string,string>** | The fields of the game&#39;s settings schema. A field left out takes its default. | [optional]
**volume** | **string** | The slug of an unused volume in the organization. Null makes a new volume named like the server. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
