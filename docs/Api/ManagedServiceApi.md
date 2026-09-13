# SomeonesComputer\Sdk\ManagedServiceApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**managedServicesCreate()**](ManagedServiceApi.md#managedServicesCreate) | **POST** /api/managed_services | Creates a ManagedService resource. |
| [**managedServicesDelete()**](ManagedServiceApi.md#managedServicesDelete) | **DELETE** /api/managed_services/{id} | Removes the ManagedService resource. |
| [**managedServicesGet()**](ManagedServiceApi.md#managedServicesGet) | **GET** /api/managed_services/{id} | Retrieves a ManagedService resource. |
| [**managedServicesList()**](ManagedServiceApi.md#managedServicesList) | **GET** /api/managed_services | Retrieves the collection of ManagedService resources. |
| [**managedServicesResume()**](ManagedServiceApi.md#managedServicesResume) | **POST** /api/managed_services/{id}/resume | Creates a ManagedService resource. |
| [**managedServicesSuspend()**](ManagedServiceApi.md#managedServicesSuspend) | **POST** /api/managed_services/{id}/suspend | Creates a ManagedService resource. |


## `managedServicesCreate()`

```php
managedServicesCreate($managed_service_managed_service_input): \SomeonesComputer\Sdk\Model\ManagedService
```

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$managed_service_managed_service_input = new \SomeonesComputer\Sdk\Model\ManagedServiceManagedServiceInput(); // \SomeonesComputer\Sdk\Model\ManagedServiceManagedServiceInput | The new ManagedService resource

try {
    $result = $apiInstance->managedServicesCreate($managed_service_managed_service_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **managed_service_managed_service_input** | [**\SomeonesComputer\Sdk\Model\ManagedServiceManagedServiceInput**](../Model/ManagedServiceManagedServiceInput.md)| The new ManagedService resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\ManagedService**](../Model/ManagedService.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedServicesDelete()`

```php
managedServicesDelete($id)
```

Removes the ManagedService resource.

Removes the ManagedService resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ManagedService identifier

try {
    $apiInstance->managedServicesDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ManagedService identifier | |

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

## `managedServicesGet()`

```php
managedServicesGet($id): \SomeonesComputer\Sdk\Model\ManagedService
```

Retrieves a ManagedService resource.

Retrieves a ManagedService resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ManagedService identifier

try {
    $result = $apiInstance->managedServicesGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ManagedService identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\ManagedService**](../Model/ManagedService.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedServicesList()`

```php
managedServicesList($page): \SomeonesComputer\Sdk\Model\ManagedService[]
```

Retrieves the collection of ManagedService resources.

Retrieves the collection of ManagedService resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->managedServicesList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\ManagedService[]**](../Model/ManagedService.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedServicesResume()`

```php
managedServicesResume($id): \SomeonesComputer\Sdk\Model\ManagedService
```

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ManagedService identifier

try {
    $result = $apiInstance->managedServicesResume($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesResume: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ManagedService identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\ManagedService**](../Model/ManagedService.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `managedServicesSuspend()`

```php
managedServicesSuspend($id): \SomeonesComputer\Sdk\Model\ManagedService
```

Creates a ManagedService resource.

Creates a ManagedService resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ManagedServiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ManagedService identifier

try {
    $result = $apiInstance->managedServicesSuspend($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesSuspend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ManagedService identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\ManagedService**](../Model/ManagedService.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
