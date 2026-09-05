# # Variable

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **string** | Re-home this variable. Used only when an application-scoped row follows its {@see Application} across organizations — an org-shared row (&#x60;$application &#x3D;&#x3D;&#x3D; null&#x60;) has no application to follow and is never moved this way. | [optional]
**application** | **string** | Null &#x3D;&gt; org-shared across all of the organization&#39;s applications. | [optional]
**key** | **string** | The environment variable name. (\&quot;key\&quot; is reserved in some SQL dialects.) | [optional]
**sensitive** | **bool** |  | [optional] [default to false]
**secret_file_delivery** | **bool** | Opt-in only, and meaningless unless {@see $sensitive} is also true: whether this secret is delivered to its containers as a mounted Swarm secret file (plus a &#x60;&lt;KEY&gt;_FILE&#x60; env var naming its path) rather than as a plain &#x60;Env&#x60; entry — {@see \\App\\Service\\Deploy\\StackDeployer}. | [optional] [default to false]
**versions** | [**\SomeonesComputer\Sdk\Model\VariableVersion[]**](VariableVersion.md) |  | [optional]
**id** | **string** |  | [optional] [readonly]
**deleted_at** | **\DateTime** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**org_shared** | **bool** |  | [optional] [readonly]
**deleted** | **bool** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
