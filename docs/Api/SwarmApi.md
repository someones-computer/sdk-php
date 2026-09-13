# SomeonesComputer\Sdk\SwarmApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**swarmsCreate()**](SwarmApi.md#swarmsCreate) | **POST** /api/swarms | Creates a Swarm resource. |
| [**swarmsDelete()**](SwarmApi.md#swarmsDelete) | **DELETE** /api/swarms/{id} | Removes the Swarm resource. |
| [**swarmsGet()**](SwarmApi.md#swarmsGet) | **GET** /api/swarms/{id} | Retrieves a Swarm resource. |
| [**swarmsList()**](SwarmApi.md#swarmsList) | **GET** /api/swarms | Retrieves the collection of Swarm resources. |
| [**swarmsUpdate()**](SwarmApi.md#swarmsUpdate) | **PATCH** /api/swarms/{id} | Updates the Swarm resource. |


## `swarmsCreate()`

```php
swarmsCreate($swarm): \SomeonesComputer\Sdk\Model\Swarm
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
    $result = $apiInstance->swarmsCreate($swarm);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->swarmsCreate: ', $e->getMessage(), PHP_EOL;
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

## `swarmsDelete()`

```php
swarmsDelete($id)
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
    $apiInstance->swarmsDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->swarmsDelete: ', $e->getMessage(), PHP_EOL;
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

## `swarmsGet()`

```php
swarmsGet($id): \SomeonesComputer\Sdk\Model\Swarm
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
    $result = $apiInstance->swarmsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->swarmsGet: ', $e->getMessage(), PHP_EOL;
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

## `swarmsList()`

```php
swarmsList($page): \SomeonesComputer\Sdk\Model\Swarm[]
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
    $result = $apiInstance->swarmsList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->swarmsList: ', $e->getMessage(), PHP_EOL;
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

## `swarmsUpdate()`

```php
swarmsUpdate($id, $swarm_json_merge_patch): \SomeonesComputer\Sdk\Model\Swarm
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
    $result = $apiInstance->swarmsUpdate($id, $swarm_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SwarmApi->swarmsUpdate: ', $e->getMessage(), PHP_EOL;
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
