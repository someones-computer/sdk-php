# SomeonesComputer\Sdk\DeploymentAccessGateApi

A per-deployment-name override of {@see Application::$accessGate} — &#x60;App\\Service\\AccessGate\\AccessGateResolver&#x60; prefers this row, keyed by &#x60;(application, name)&#x60;, over the application&#39;s own default whenever one exists for the deployment name being resolved. &#x60;$name&#x60; matches {@see Deployment::$name}: a branch/environment, not one immutable revision, so redeploying the same branch keeps whatever gate was set for it.  Absence, not a &#x60;None&#x60; row, is what \&quot;inherit the application default\&quot; means — &#x60;App\\Service\\AccessGate\\AccessGateModeSwitcher::clearOverride()&#x60; deletes the row rather than setting its mode to &#x60;None&#x60;, so a later change to the application&#39;s own default is picked up by every deployment that never overrode it.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deploymentAccessGatesCreate()**](DeploymentAccessGateApi.md#deploymentAccessGatesCreate) | **POST** /api/deployment_access_gates | Creates a DeploymentAccessGate resource. |
| [**deploymentAccessGatesDelete()**](DeploymentAccessGateApi.md#deploymentAccessGatesDelete) | **DELETE** /api/deployment_access_gates/{id} | Removes the DeploymentAccessGate resource. |
| [**deploymentAccessGatesGet()**](DeploymentAccessGateApi.md#deploymentAccessGatesGet) | **GET** /api/deployment_access_gates/{id} | Retrieves a DeploymentAccessGate resource. |
| [**deploymentAccessGatesList()**](DeploymentAccessGateApi.md#deploymentAccessGatesList) | **GET** /api/deployment_access_gates | Retrieves the collection of DeploymentAccessGate resources. |
| [**deploymentAccessGatesUpdate()**](DeploymentAccessGateApi.md#deploymentAccessGatesUpdate) | **PATCH** /api/deployment_access_gates/{id} | Updates the DeploymentAccessGate resource. |


## `deploymentAccessGatesCreate()`

```php
deploymentAccessGatesCreate($deployment_access_gate): \SomeonesComputer\Sdk\Model\DeploymentAccessGate
```

Creates a DeploymentAccessGate resource.

Creates a DeploymentAccessGate resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentAccessGateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$deployment_access_gate = new \SomeonesComputer\Sdk\Model\DeploymentAccessGate(); // \SomeonesComputer\Sdk\Model\DeploymentAccessGate | The new DeploymentAccessGate resource

try {
    $result = $apiInstance->deploymentAccessGatesCreate($deployment_access_gate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentAccessGateApi->deploymentAccessGatesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **deployment_access_gate** | [**\SomeonesComputer\Sdk\Model\DeploymentAccessGate**](../Model/DeploymentAccessGate.md)| The new DeploymentAccessGate resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentAccessGate**](../Model/DeploymentAccessGate.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deploymentAccessGatesDelete()`

```php
deploymentAccessGatesDelete($id)
```

Removes the DeploymentAccessGate resource.

Removes the DeploymentAccessGate resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentAccessGateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | DeploymentAccessGate identifier

try {
    $apiInstance->deploymentAccessGatesDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentAccessGateApi->deploymentAccessGatesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| DeploymentAccessGate identifier | |

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

## `deploymentAccessGatesGet()`

```php
deploymentAccessGatesGet($id): \SomeonesComputer\Sdk\Model\DeploymentAccessGate
```

Retrieves a DeploymentAccessGate resource.

Retrieves a DeploymentAccessGate resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentAccessGateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | DeploymentAccessGate identifier

try {
    $result = $apiInstance->deploymentAccessGatesGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentAccessGateApi->deploymentAccessGatesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| DeploymentAccessGate identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentAccessGate**](../Model/DeploymentAccessGate.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deploymentAccessGatesList()`

```php
deploymentAccessGatesList($page): \SomeonesComputer\Sdk\Model\DeploymentAccessGate[]
```

Retrieves the collection of DeploymentAccessGate resources.

Retrieves the collection of DeploymentAccessGate resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentAccessGateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->deploymentAccessGatesList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentAccessGateApi->deploymentAccessGatesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentAccessGate[]**](../Model/DeploymentAccessGate.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deploymentAccessGatesUpdate()`

```php
deploymentAccessGatesUpdate($id, $deployment_access_gate_json_merge_patch): \SomeonesComputer\Sdk\Model\DeploymentAccessGate
```

Updates the DeploymentAccessGate resource.

Updates the DeploymentAccessGate resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\DeploymentAccessGateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | DeploymentAccessGate identifier
$deployment_access_gate_json_merge_patch = new \SomeonesComputer\Sdk\Model\DeploymentAccessGateJsonMergePatch(); // \SomeonesComputer\Sdk\Model\DeploymentAccessGateJsonMergePatch | The updated DeploymentAccessGate resource

try {
    $result = $apiInstance->deploymentAccessGatesUpdate($id, $deployment_access_gate_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentAccessGateApi->deploymentAccessGatesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| DeploymentAccessGate identifier | |
| **deployment_access_gate_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\DeploymentAccessGateJsonMergePatch**](../Model/DeploymentAccessGateJsonMergePatch.md)| The updated DeploymentAccessGate resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\DeploymentAccessGate**](../Model/DeploymentAccessGate.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
