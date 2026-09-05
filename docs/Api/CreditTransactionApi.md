# SomeonesComputer\Sdk\CreditTransactionApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiCreditTransactionsGetCollection()**](CreditTransactionApi.md#apiCreditTransactionsGetCollection) | **GET** /api/credit_transactions | Retrieves the collection of CreditTransaction resources. |
| [**apiCreditTransactionsIdGet()**](CreditTransactionApi.md#apiCreditTransactionsIdGet) | **GET** /api/credit_transactions/{id} | Retrieves a CreditTransaction resource. |


## `apiCreditTransactionsGetCollection()`

```php
apiCreditTransactionsGetCollection($page): \SomeonesComputer\Sdk\Model\CreditTransaction[]
```

Retrieves the collection of CreditTransaction resources.

Retrieves the collection of CreditTransaction resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\CreditTransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiCreditTransactionsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditTransactionApi->apiCreditTransactionsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\CreditTransaction[]**](../Model/CreditTransaction.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiCreditTransactionsIdGet()`

```php
apiCreditTransactionsIdGet($id): \SomeonesComputer\Sdk\Model\CreditTransaction
```

Retrieves a CreditTransaction resource.

Retrieves a CreditTransaction resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\CreditTransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | CreditTransaction identifier

try {
    $result = $apiInstance->apiCreditTransactionsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditTransactionApi->apiCreditTransactionsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| CreditTransaction identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\CreditTransaction**](../Model/CreditTransaction.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
