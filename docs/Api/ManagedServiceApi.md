# SomeonesComputer\Sdk\ManagedServiceApi

One tenant&#39;s database or bucket on a shared engine.  **Owned by an organization and bound to applications** — not a per-application toggle. The distinction is the whole reason this entity exists in this shape: a toggle with a unique foreign key cannot express one database backing both a web app and its worker, and cannot survive an application being rebuilt under a new name. Binding is therefore explicit ({@see ServiceBinding}), which costs one step at creation and buys sharing, one billing shape, one permission model and one set of verbs across databases *and* buckets.  A bucket is the same noun with a different {@see $kind}. Only the driver that executes the tenancy operations differs.  Soft-deleted, so a destroy is recoverable within its grace period ({@see ManagedServiceRepository::GRACE_PERIOD}); only the driver&#39;s &#x60;DROP&#x60; is not, and that runs on the far side of it.  **Read is scoped by membership and writing by role**, which are different questions: {@see \\App\\ApiResource\\ManagedServiceOwnerExtension} filters the query, so another tenant&#39;s id answers 404 rather than confirming it exists, while {@see \\App\\Security\\Voter\\ManageVoter} governs the verbs inside each processor — a plain member may see their organization&#39;s databases without being able to destroy one.  Delete does *not* fall through to the generic soft-delete processor: dropping a database is not stamping a column, and the difference is a tenant&#39;s data. See {@see \\App\\State\\ManagedServiceDestroyProcessor}.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**managedServicesCreate()**](ManagedServiceApi.md#managedServicesCreate) | **POST** /api/managed_services | Creates a ManagedService resource. |
| [**managedServicesDelete()**](ManagedServiceApi.md#managedServicesDelete) | **DELETE** /api/managed_services/{id} | Removes the ManagedService resource. |
| [**managedServicesGet()**](ManagedServiceApi.md#managedServicesGet) | **GET** /api/managed_services/{id} | Retrieves a ManagedService resource. |
| [**managedServicesList()**](ManagedServiceApi.md#managedServicesList) | **GET** /api/managed_services | Retrieves the collection of ManagedService resources. |
| [**managedServicesListRetired()**](ManagedServiceApi.md#managedServicesListRetired) | **GET** /api/managed_services/retired | Retrieves the collection of ManagedService resources. |
| [**managedServicesRestore()**](ManagedServiceApi.md#managedServicesRestore) | **POST** /api/managed_services/{id}/restore | Creates a ManagedService resource. |
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

## `managedServicesListRetired()`

```php
managedServicesListRetired(): \SomeonesComputer\Sdk\Model\ManagedService[]
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

try {
    $result = $apiInstance->managedServicesListRetired();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesListRetired: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `managedServicesRestore()`

```php
managedServicesRestore($id): \SomeonesComputer\Sdk\Model\ManagedService
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
    $result = $apiInstance->managedServicesRestore($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagedServiceApi->managedServicesRestore: ', $e->getMessage(), PHP_EOL;
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
