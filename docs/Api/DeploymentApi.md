# SomeonesComputer\Sdk\DeploymentApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiDeploymentsGetCollection()**](DeploymentApi.md#apiDeploymentsGetCollection) | **GET** /api/deployments | Retrieves the collection of Deployment resources. |
| [**apiDeploymentsIdDelete()**](DeploymentApi.md#apiDeploymentsIdDelete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource. |
| [**apiDeploymentsIdGet()**](DeploymentApi.md#apiDeploymentsIdGet) | **GET** /api/deployments/{id} | Retrieves a Deployment resource. |
| [**apiDeploymentsIdPatch()**](DeploymentApi.md#apiDeploymentsIdPatch) | **PATCH** /api/deployments/{id} | Updates the Deployment resource. |
| [**apiDeploymentsPost()**](DeploymentApi.md#apiDeploymentsPost) | **POST** /api/deployments | Creates a Deployment resource. |


## `apiDeploymentsGetCollection()`

```php
apiDeploymentsGetCollection($page): \SomeonesComputer\Sdk\Model\Deployment[]
```

Retrieves the collection of Deployment resources.

Retrieves the collection of Deployment resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiDeploymentsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\Deployment[]**](../Model/Deployment.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDeploymentsIdDelete()`

```php
apiDeploymentsIdDelete($id)
```

Removes the Deployment resource.

Removes the Deployment resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Deployment identifier

try {
    $apiInstance->apiDeploymentsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Deployment identifier | |

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

## `apiDeploymentsIdGet()`

```php
apiDeploymentsIdGet($id): \SomeonesComputer\Sdk\Model\Deployment
```

Retrieves a Deployment resource.

Retrieves a Deployment resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Deployment identifier

try {
    $result = $apiInstance->apiDeploymentsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Deployment identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\Deployment**](../Model/Deployment.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDeploymentsIdPatch()`

```php
apiDeploymentsIdPatch($id, $deployment_json_merge_patch): \SomeonesComputer\Sdk\Model\Deployment
```

Updates the Deployment resource.

Updates the Deployment resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Deployment identifier
$deployment_json_merge_patch = new \SomeonesComputer\Sdk\Model\DeploymentJsonMergePatch(); // \SomeonesComputer\Sdk\Model\DeploymentJsonMergePatch | The updated Deployment resource

try {
    $result = $apiInstance->apiDeploymentsIdPatch($id, $deployment_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Deployment identifier | |
| **deployment_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\DeploymentJsonMergePatch**](../Model/DeploymentJsonMergePatch.md)| The updated Deployment resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Deployment**](../Model/Deployment.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDeploymentsPost()`

```php
apiDeploymentsPost($deployment): \SomeonesComputer\Sdk\Model\Deployment
```

Creates a Deployment resource.

Creates a Deployment resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$deployment = new \SomeonesComputer\Sdk\Model\Deployment(); // \SomeonesComputer\Sdk\Model\Deployment | The new Deployment resource

try {
    $result = $apiInstance->apiDeploymentsPost($deployment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deployment** | [**\SomeonesComputer\Sdk\Model\Deployment**](../Model/Deployment.md)| The new Deployment resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Deployment**](../Model/Deployment.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
