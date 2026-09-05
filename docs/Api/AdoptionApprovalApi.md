# SomeonesComputer\Sdk\AdoptionApprovalApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiAdoptionApprovalsGetCollection()**](AdoptionApprovalApi.md#apiAdoptionApprovalsGetCollection) | **GET** /api/adoption_approvals | Retrieves the collection of AdoptionApproval resources. |
| [**apiAdoptionApprovalsIdDelete()**](AdoptionApprovalApi.md#apiAdoptionApprovalsIdDelete) | **DELETE** /api/adoption_approvals/{id} | Removes the AdoptionApproval resource. |
| [**apiAdoptionApprovalsIdGet()**](AdoptionApprovalApi.md#apiAdoptionApprovalsIdGet) | **GET** /api/adoption_approvals/{id} | Retrieves a AdoptionApproval resource. |
| [**apiAdoptionApprovalsPost()**](AdoptionApprovalApi.md#apiAdoptionApprovalsPost) | **POST** /api/adoption_approvals | Creates a AdoptionApproval resource. |


## `apiAdoptionApprovalsGetCollection()`

```php
apiAdoptionApprovalsGetCollection($page): \SomeonesComputer\Sdk\Model\AdoptionApproval[]
```

Retrieves the collection of AdoptionApproval resources.

Retrieves the collection of AdoptionApproval resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\AdoptionApprovalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiAdoptionApprovalsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->apiAdoptionApprovalsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\AdoptionApproval[]**](../Model/AdoptionApproval.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiAdoptionApprovalsIdDelete()`

```php
apiAdoptionApprovalsIdDelete($id)
```

Removes the AdoptionApproval resource.

Removes the AdoptionApproval resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\AdoptionApprovalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | AdoptionApproval identifier

try {
    $apiInstance->apiAdoptionApprovalsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->apiAdoptionApprovalsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| AdoptionApproval identifier | |

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

## `apiAdoptionApprovalsIdGet()`

```php
apiAdoptionApprovalsIdGet($id): \SomeonesComputer\Sdk\Model\AdoptionApproval
```

Retrieves a AdoptionApproval resource.

Retrieves a AdoptionApproval resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\AdoptionApprovalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | AdoptionApproval identifier

try {
    $result = $apiInstance->apiAdoptionApprovalsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->apiAdoptionApprovalsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| AdoptionApproval identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\AdoptionApproval**](../Model/AdoptionApproval.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiAdoptionApprovalsPost()`

```php
apiAdoptionApprovalsPost($adoption_approval_adoption_approval_input): \SomeonesComputer\Sdk\Model\AdoptionApproval
```

Creates a AdoptionApproval resource.

Creates a AdoptionApproval resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\AdoptionApprovalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$adoption_approval_adoption_approval_input = new \SomeonesComputer\Sdk\Model\AdoptionApprovalAdoptionApprovalInput(); // \SomeonesComputer\Sdk\Model\AdoptionApprovalAdoptionApprovalInput | The new AdoptionApproval resource

try {
    $result = $apiInstance->apiAdoptionApprovalsPost($adoption_approval_adoption_approval_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->apiAdoptionApprovalsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **adoption_approval_adoption_approval_input** | [**\SomeonesComputer\Sdk\Model\AdoptionApprovalAdoptionApprovalInput**](../Model/AdoptionApprovalAdoptionApprovalInput.md)| The new AdoptionApproval resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\AdoptionApproval**](../Model/AdoptionApproval.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
