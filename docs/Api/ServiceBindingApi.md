# SomeonesComputer\Sdk\ServiceBindingApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiServiceBindingsGetCollection()**](ServiceBindingApi.md#apiServiceBindingsGetCollection) | **GET** /api/service_bindings | Retrieves the collection of ServiceBinding resources. |
| [**apiServiceBindingsIdDelete()**](ServiceBindingApi.md#apiServiceBindingsIdDelete) | **DELETE** /api/service_bindings/{id} | Removes the ServiceBinding resource. |
| [**apiServiceBindingsIdGet()**](ServiceBindingApi.md#apiServiceBindingsIdGet) | **GET** /api/service_bindings/{id} | Retrieves a ServiceBinding resource. |
| [**apiServiceBindingsPost()**](ServiceBindingApi.md#apiServiceBindingsPost) | **POST** /api/service_bindings | Creates a ServiceBinding resource. |


## `apiServiceBindingsGetCollection()`

```php
apiServiceBindingsGetCollection($page): \SomeonesComputer\Sdk\Model\ServiceBinding[]
```

Retrieves the collection of ServiceBinding resources.

Retrieves the collection of ServiceBinding resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ServiceBindingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiServiceBindingsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceBindingApi->apiServiceBindingsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\ServiceBinding[]**](../Model/ServiceBinding.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiServiceBindingsIdDelete()`

```php
apiServiceBindingsIdDelete($id)
```

Removes the ServiceBinding resource.

Removes the ServiceBinding resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ServiceBindingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ServiceBinding identifier

try {
    $apiInstance->apiServiceBindingsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling ServiceBindingApi->apiServiceBindingsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ServiceBinding identifier | |

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

## `apiServiceBindingsIdGet()`

```php
apiServiceBindingsIdGet($id): \SomeonesComputer\Sdk\Model\ServiceBinding
```

Retrieves a ServiceBinding resource.

Retrieves a ServiceBinding resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ServiceBindingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ServiceBinding identifier

try {
    $result = $apiInstance->apiServiceBindingsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceBindingApi->apiServiceBindingsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ServiceBinding identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\ServiceBinding**](../Model/ServiceBinding.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiServiceBindingsPost()`

```php
apiServiceBindingsPost($service_binding_service_binding_input): \SomeonesComputer\Sdk\Model\ServiceBinding
```

Creates a ServiceBinding resource.

Creates a ServiceBinding resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ServiceBindingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$service_binding_service_binding_input = new \SomeonesComputer\Sdk\Model\ServiceBindingServiceBindingInput(); // \SomeonesComputer\Sdk\Model\ServiceBindingServiceBindingInput | The new ServiceBinding resource

try {
    $result = $apiInstance->apiServiceBindingsPost($service_binding_service_binding_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceBindingApi->apiServiceBindingsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **service_binding_service_binding_input** | [**\SomeonesComputer\Sdk\Model\ServiceBindingServiceBindingInput**](../Model/ServiceBindingServiceBindingInput.md)| The new ServiceBinding resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\ServiceBinding**](../Model/ServiceBinding.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
