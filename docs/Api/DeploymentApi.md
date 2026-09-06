# SomeonesComputer\Sdk\DeploymentApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiDeploymentsGetCollection()**](DeploymentApi.md#apiDeploymentsGetCollection) | **GET** /api/deployments | Retrieves the collection of Deployment resources. |
| [**apiDeploymentsIdDelete()**](DeploymentApi.md#apiDeploymentsIdDelete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource. |
| [**apiDeploymentsIdGet()**](DeploymentApi.md#apiDeploymentsIdGet) | **GET** /api/deployments/{id} | Retrieves a Deployment resource. |
| [**apiDeploymentsIdPatch()**](DeploymentApi.md#apiDeploymentsIdPatch) | **PATCH** /api/deployments/{id} | Updates the Deployment resource. |
| [**apiDeploymentsIdendpointsGetCollection()**](DeploymentApi.md#apiDeploymentsIdendpointsGetCollection) | **GET** /api/deployments/{id}/endpoints | Retrieves the collection of Deployment resources. |
| [**apiDeploymentsPost()**](DeploymentApi.md#apiDeploymentsPost) | **POST** /api/deployments | Creates a Deployment resource. |
| [**bundleUploadConfirm()**](DeploymentApi.md#bundleUploadConfirm) | **POST** /api/deployments/bundle_uploads/confirm | Creates a Deployment resource. |
| [**bundleUploadDeclare()**](DeploymentApi.md#bundleUploadDeclare) | **POST** /api/deployments/bundle_uploads | Creates a Deployment resource. |


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

## `apiDeploymentsIdendpointsGetCollection()`

```php
apiDeploymentsIdendpointsGetCollection($id): \SomeonesComputer\Sdk\Model\DeploymentDeploymentEndpoint[]
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
$id = 'id_example'; // string | Deployment identifier

try {
    $result = $apiInstance->apiDeploymentsIdendpointsGetCollection($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->apiDeploymentsIdendpointsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Deployment identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentDeploymentEndpoint[]**](../Model/DeploymentDeploymentEndpoint.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

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

## `bundleUploadConfirm()`

```php
bundleUploadConfirm($deployment_bundle_upload_confirm_input): \SomeonesComputer\Sdk\Model\DeploymentBundleUploadConfirmOutput
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
$deployment_bundle_upload_confirm_input = new \SomeonesComputer\Sdk\Model\DeploymentBundleUploadConfirmInput(); // \SomeonesComputer\Sdk\Model\DeploymentBundleUploadConfirmInput | The new Deployment resource

try {
    $result = $apiInstance->bundleUploadConfirm($deployment_bundle_upload_confirm_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->bundleUploadConfirm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deployment_bundle_upload_confirm_input** | [**\SomeonesComputer\Sdk\Model\DeploymentBundleUploadConfirmInput**](../Model/DeploymentBundleUploadConfirmInput.md)| The new Deployment resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentBundleUploadConfirmOutput**](../Model/DeploymentBundleUploadConfirmOutput.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bundleUploadDeclare()`

```php
bundleUploadDeclare($deployment_bundle_upload_declare_input): \SomeonesComputer\Sdk\Model\DeploymentBundleUploadDeclareOutput
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
$deployment_bundle_upload_declare_input = new \SomeonesComputer\Sdk\Model\DeploymentBundleUploadDeclareInput(); // \SomeonesComputer\Sdk\Model\DeploymentBundleUploadDeclareInput | The new Deployment resource

try {
    $result = $apiInstance->bundleUploadDeclare($deployment_bundle_upload_declare_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentApi->bundleUploadDeclare: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deployment_bundle_upload_declare_input** | [**\SomeonesComputer\Sdk\Model\DeploymentBundleUploadDeclareInput**](../Model/DeploymentBundleUploadDeclareInput.md)| The new Deployment resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentBundleUploadDeclareOutput**](../Model/DeploymentBundleUploadDeclareOutput.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
