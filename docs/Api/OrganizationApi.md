# SomeonesComputer\Sdk\OrganizationApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiOrganizationsGetCollection()**](OrganizationApi.md#apiOrganizationsGetCollection) | **GET** /api/organizations | Retrieves the collection of Organization resources. |
| [**apiOrganizationsIdDelete()**](OrganizationApi.md#apiOrganizationsIdDelete) | **DELETE** /api/organizations/{id} | Removes the Organization resource. |
| [**apiOrganizationsIdGet()**](OrganizationApi.md#apiOrganizationsIdGet) | **GET** /api/organizations/{id} | Retrieves a Organization resource. |
| [**apiOrganizationsIdPatch()**](OrganizationApi.md#apiOrganizationsIdPatch) | **PATCH** /api/organizations/{id} | Updates the Organization resource. |
| [**apiOrganizationsPost()**](OrganizationApi.md#apiOrganizationsPost) | **POST** /api/organizations | Creates a Organization resource. |


## `apiOrganizationsGetCollection()`

```php
apiOrganizationsGetCollection($page, $slug, $slug2): \SomeonesComputer\Sdk\Model\Organization[]
```

Retrieves the collection of Organization resources.

Retrieves the collection of Organization resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number
$slug = 'slug_example'; // string | 
$slug2 = array('slug_example'); // string[] | 

try {
    $result = $apiInstance->apiOrganizationsGetCollection($page, $slug, $slug2);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->apiOrganizationsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |
| **slug** | **string**|  | [optional] |
| **slug2** | [**string[]**](../Model/string.md)|  | [optional] |

### Return type

[**\SomeonesComputer\Sdk\Model\Organization[]**](../Model/Organization.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiOrganizationsIdDelete()`

```php
apiOrganizationsIdDelete($id)
```

Removes the Organization resource.

Removes the Organization resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Organization identifier

try {
    $apiInstance->apiOrganizationsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->apiOrganizationsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Organization identifier | |

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

## `apiOrganizationsIdGet()`

```php
apiOrganizationsIdGet($id): \SomeonesComputer\Sdk\Model\Organization
```

Retrieves a Organization resource.

Retrieves a Organization resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Organization identifier

try {
    $result = $apiInstance->apiOrganizationsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->apiOrganizationsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Organization identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\Organization**](../Model/Organization.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiOrganizationsIdPatch()`

```php
apiOrganizationsIdPatch($id, $organization_json_merge_patch): \SomeonesComputer\Sdk\Model\Organization
```

Updates the Organization resource.

Updates the Organization resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Organization identifier
$organization_json_merge_patch = new \SomeonesComputer\Sdk\Model\OrganizationJsonMergePatch(); // \SomeonesComputer\Sdk\Model\OrganizationJsonMergePatch | The updated Organization resource

try {
    $result = $apiInstance->apiOrganizationsIdPatch($id, $organization_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->apiOrganizationsIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Organization identifier | |
| **organization_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\OrganizationJsonMergePatch**](../Model/OrganizationJsonMergePatch.md)| The updated Organization resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Organization**](../Model/Organization.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiOrganizationsPost()`

```php
apiOrganizationsPost($organization): \SomeonesComputer\Sdk\Model\Organization
```

Creates a Organization resource.

Creates a Organization resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\OrganizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = new \SomeonesComputer\Sdk\Model\Organization(); // \SomeonesComputer\Sdk\Model\Organization | The new Organization resource

try {
    $result = $apiInstance->apiOrganizationsPost($organization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationApi->apiOrganizationsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | [**\SomeonesComputer\Sdk\Model\Organization**](../Model/Organization.md)| The new Organization resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Organization**](../Model/Organization.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
