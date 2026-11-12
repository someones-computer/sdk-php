# SomeonesComputer\Sdk\ApplicationVolumeApi

A named volume that a compose file declares, kept on one swarm node for one stack of one application (docs/named-volumes.md).  Not {@see Volume}. That one is an organization&#39;s S3 bucket for a game server. This one is a Docker &#x60;local&#x60; volume: the bytes sit on the node&#39;s disk, so the row records which node, and {@see \\App\\Service\\Volume\\NamedVolumes} pins the owning service there.  **The Docker name is &#x60;&lt;stack&gt;_&lt;name&gt;&#x60;** ({@see self::dockerName()}). The stack name carries the environment prefix, the organization and the application, so two applications that both declare &#x60;data&#x60; get two volumes. The row exists from the first deploy that mounts the volume. A redeploy finds it again by that name and reuses it. Nothing but an explicit delete ({@see ApplicationVolumeDeleteProcessor}, &#x60;delete_application_volume&#x60;) removes it.  The API shows a volume and deletes it. It never creates one: the compose file does that. The operations show in the OpenAPI document and in the four generated SDKs.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiApplicationVolumesGetCollection()**](ApplicationVolumeApi.md#apiApplicationVolumesGetCollection) | **GET** /api/application_volumes | Retrieves the collection of ApplicationVolume resources. |
| [**apiApplicationVolumesIdDelete()**](ApplicationVolumeApi.md#apiApplicationVolumesIdDelete) | **DELETE** /api/application_volumes/{id} | Removes the ApplicationVolume resource. |
| [**apiApplicationVolumesIdGet()**](ApplicationVolumeApi.md#apiApplicationVolumesIdGet) | **GET** /api/application_volumes/{id} | Retrieves a ApplicationVolume resource. |


## `apiApplicationVolumesGetCollection()`

```php
apiApplicationVolumesGetCollection($page): \SomeonesComputer\Sdk\Model\ApplicationVolume[]
```

Retrieves the collection of ApplicationVolume resources.

Retrieves the collection of ApplicationVolume resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationVolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiApplicationVolumesGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationVolumeApi->apiApplicationVolumesGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\ApplicationVolume[]**](../Model/ApplicationVolume.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiApplicationVolumesIdDelete()`

```php
apiApplicationVolumesIdDelete($id)
```

Removes the ApplicationVolume resource.

Removes the ApplicationVolume resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationVolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ApplicationVolume identifier

try {
    $apiInstance->apiApplicationVolumesIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationVolumeApi->apiApplicationVolumesIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ApplicationVolume identifier | |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/problem+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiApplicationVolumesIdGet()`

```php
apiApplicationVolumesIdGet($id): \SomeonesComputer\Sdk\Model\ApplicationVolume
```

Retrieves a ApplicationVolume resource.

Retrieves a ApplicationVolume resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationVolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ApplicationVolume identifier

try {
    $result = $apiInstance->apiApplicationVolumesIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationVolumeApi->apiApplicationVolumesIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ApplicationVolume identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\ApplicationVolume**](../Model/ApplicationVolume.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
