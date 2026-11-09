# GameServerGameServerRead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **string** |  | [optional]
**slug** | **string** |  | [optional]
**name** | **string** |  | [optional]
**kind** | **string** |  | [optional]
**version** | **string** |  | [optional]
**settings** | [**array<string,\SomeonesComputer\Sdk\Model\GameServerGameServerReadSettingsValue>**](GameServerGameServerReadSettingsValue.md) |  | [optional]
**state** | **string** | The reason only means something for &#x60;failed&#x60;, so any other state clears it. | [optional] [default to 'stopped']
**state_reason** | **string** | Why the server is &#x60;failed&#x60;, in words a tenant can read. Null in every other state. | [optional] [readonly]
**volume** | **string** | The volume&#39;s slug, so a client can name the world without the bucket behind it. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
