# SomeonesComputer\Sdk\SwarmApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiSwarmsGetCollection()**](SwarmApi.md#apiSwarmsGetCollection) | **GET** /api/swarms | Retrieves the collection of Swarm resources. |
| [**apiSwarmsIdDelete()**](SwarmApi.md#apiSwarmsIdDelete) | **DELETE** /api/swarms/{id} | Removes the Swarm resource. |
| [**apiSwarmsIdGet()**](SwarmApi.md#apiSwarmsIdGet) | **GET** /api/swarms/{id} | Retrieves a Swarm resource. |
| [**apiSwarmsIdPatch()**](SwarmApi.md#apiSwarmsIdPatch) | **PATCH** /api/swarms/{id} | Updates the Swarm resource. |
| [**apiSwarmsPost()**](SwarmApi.md#apiSwarmsPost) | **POST** /api/swarms | Creates a Swarm resource. |


## `apiSwarmsGetCollection()`

```php
apiSwarmsGetCollection($page): \SomeonesComputer\Sdk\Model\Swarm[]
```

Retrieves the collection of Swarm resources.

Retrieves the collection of Swarm resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\SwarmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiSwarmsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->apiSwarmsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\Swarm[]**](../Model/Swarm.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiSwarmsIdDelete()`

```php
apiSwarmsIdDelete($id)
```

Removes the Swarm resource.

Removes the Swarm resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\SwarmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Swarm identifier

try {
    $apiInstance->apiSwarmsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->apiSwarmsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Swarm identifier | |

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

## `apiSwarmsIdGet()`

```php
apiSwarmsIdGet($id): \SomeonesComputer\Sdk\Model\Swarm
```

Retrieves a Swarm resource.

Retrieves a Swarm resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\SwarmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Swarm identifier

try {
    $result = $apiInstance->apiSwarmsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->apiSwarmsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Swarm identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\Swarm**](../Model/Swarm.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiSwarmsIdPatch()`

```php
apiSwarmsIdPatch($id, $swarm_json_merge_patch): \SomeonesComputer\Sdk\Model\Swarm
```

Updates the Swarm resource.

Updates the Swarm resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\SwarmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Swarm identifier
$swarm_json_merge_patch = new \SomeonesComputer\Sdk\Model\SwarmJsonMergePatch(); // \SomeonesComputer\Sdk\Model\SwarmJsonMergePatch | The updated Swarm resource

try {
    $result = $apiInstance->apiSwarmsIdPatch($id, $swarm_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->apiSwarmsIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Swarm identifier | |
| **swarm_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\SwarmJsonMergePatch**](../Model/SwarmJsonMergePatch.md)| The updated Swarm resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Swarm**](../Model/Swarm.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiSwarmsPost()`

```php
apiSwarmsPost($swarm): \SomeonesComputer\Sdk\Model\Swarm
```

Creates a Swarm resource.

Creates a Swarm resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\SwarmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$swarm = new \SomeonesComputer\Sdk\Model\Swarm(); // \SomeonesComputer\Sdk\Model\Swarm | The new Swarm resource

try {
    $result = $apiInstance->apiSwarmsPost($swarm);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->apiSwarmsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **swarm** | [**\SomeonesComputer\Sdk\Model\Swarm**](../Model/Swarm.md)| The new Swarm resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Swarm**](../Model/Swarm.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
