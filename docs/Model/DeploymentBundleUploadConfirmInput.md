# # DeploymentBundleUploadConfirmInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**secrets** | **array<string,array<string,string>>** | Raw &#x60;build.secrets&#x60; values, keyed by service then by BuildKit secret id (Grey.ooo/someones.computer_agent#46) — matches &#x60;App\\Service\\Bundle\\BundleIngestor::commitFromStoredContent()&#x60;&#39;s &#x60;$secrets&#x60; parameter. | [optional]
**application** | **string** |  |
**client** | **string** | Matches &#x60;App\\Service\\Bundle\\BundleManifest::$client&#x60; — which client produced this. | [default to 'api']
**name** | **string** |  | [optional]
**force** | **bool** | Ask for a new revision even if this digest already matches one — {@see BundleManifest::$force}&#39;s own meaning, unchanged. | [optional] [default to false]
**compose** | **string** |  | [default to '']
**contexts** | [**\SomeonesComputer\Sdk\Model\BundleContextInput[]**](BundleContextInput.md) |  | [optional]
**images** | [**\SomeonesComputer\Sdk\Model\BundleForwardedImageInput[]**](BundleForwardedImageInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
