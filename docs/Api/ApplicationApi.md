# SomeonesComputer\Sdk\ApplicationApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiApplicationsGetCollection()**](ApplicationApi.md#apiApplicationsGetCollection) | **GET** /api/applications | Retrieves the collection of Application resources. |
| [**apiApplicationsIdDelete()**](ApplicationApi.md#apiApplicationsIdDelete) | **DELETE** /api/applications/{id} | Removes the Application resource. |
| [**apiApplicationsIdGet()**](ApplicationApi.md#apiApplicationsIdGet) | **GET** /api/applications/{id} | Retrieves a Application resource. |
| [**apiApplicationsIdPatch()**](ApplicationApi.md#apiApplicationsIdPatch) | **PATCH** /api/applications/{id} | Updates the Application resource. |
| [**apiApplicationsPost()**](ApplicationApi.md#apiApplicationsPost) | **POST** /api/applications | Creates a Application resource. |


## `apiApplicationsGetCollection()`

```php
apiApplicationsGetCollection($page, $slug, $slug2, $organization, $organization2, $organization_slug, $organization_slug2): \SomeonesComputer\Sdk\Model\Application[]
```

Retrieves the collection of Application resources.

Retrieves the collection of Application resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number
$slug = 'slug_example'; // string | 
$slug2 = array('slug_example'); // string[] | 
$organization = 'organization_example'; // string | 
$organization2 = array('organization_example'); // string[] | 
$organization_slug = 'organization_slug_example'; // string | 
$organization_slug2 = array('organization_slug_example'); // string[] | 

try {
    $result = $apiInstance->apiApplicationsGetCollection($page, $slug, $slug2, $organization, $organization2, $organization_slug, $organization_slug2);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->apiApplicationsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |
| **slug** | **string**|  | [optional] |
| **slug2** | [**string[]**](../Model/string.md)|  | [optional] |
| **organization** | **string**|  | [optional] |
| **organization2** | [**string[]**](../Model/string.md)|  | [optional] |
| **organization_slug** | **string**|  | [optional] |
| **organization_slug2** | [**string[]**](../Model/string.md)|  | [optional] |

### Return type

[**\SomeonesComputer\Sdk\Model\Application[]**](../Model/Application.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiApplicationsIdDelete()`

```php
apiApplicationsIdDelete($id)
```

Removes the Application resource.

Removes the Application resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Application identifier

try {
    $apiInstance->apiApplicationsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->apiApplicationsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Application identifier | |

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

## `apiApplicationsIdGet()`

```php
apiApplicationsIdGet($id): \SomeonesComputer\Sdk\Model\Application
```

Retrieves a Application resource.

Retrieves a Application resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Application identifier

try {
    $result = $apiInstance->apiApplicationsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->apiApplicationsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Application identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\Application**](../Model/Application.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiApplicationsIdPatch()`

```php
apiApplicationsIdPatch($id, $application_json_merge_patch): \SomeonesComputer\Sdk\Model\Application
```

Updates the Application resource.

Updates the Application resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Application identifier
$application_json_merge_patch = new \SomeonesComputer\Sdk\Model\ApplicationJsonMergePatch(); // \SomeonesComputer\Sdk\Model\ApplicationJsonMergePatch | The updated Application resource

try {
    $result = $apiInstance->apiApplicationsIdPatch($id, $application_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->apiApplicationsIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Application identifier | |
| **application_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\ApplicationJsonMergePatch**](../Model/ApplicationJsonMergePatch.md)| The updated Application resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Application**](../Model/Application.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiApplicationsPost()`

```php
apiApplicationsPost($application): \SomeonesComputer\Sdk\Model\Application
```

Creates a Application resource.

Creates a Application resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\ApplicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$application = new \SomeonesComputer\Sdk\Model\Application(); // \SomeonesComputer\Sdk\Model\Application | The new Application resource

try {
    $result = $apiInstance->apiApplicationsPost($application);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationApi->apiApplicationsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **application** | [**\SomeonesComputer\Sdk\Model\Application**](../Model/Application.md)| The new Application resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Application**](../Model/Application.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
