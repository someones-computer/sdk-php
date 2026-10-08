# SomeonesComputer\Sdk\CreditTransactionApi

An IMMUTABLE, append-only ledger row for an Organization&#39;s shared credit balance. A balance is never mutated in place — it&#39;s always &#x60;SUM(amountCents)&#x60; over &#x60;Succeeded&#x60; rows (see {@see CreditTransactionRepository::balanceForOrganization()}). Read-only over the API: money movement stays server-driven.  Three kinds of row, one table ({@see CreditTransactionType}):    - a **top-up** is created &#x60;Pending&#x60; before redirecting to Stripe Checkout,     keyed on &#x60;stripeCheckoutSessionId&#x60;, then flipped to &#x60;Succeeded&#x60;/&#x60;Failed&#x60;     by {@see \\App\\Controller\\StripeWebhookController};   - a **grant** and a **debit** are terminal the moment they are written, so     both are written &#x60;Succeeded&#x60; — the &#x60;Pending&#x60; default is a Stripe-webhook     state and is wrong for them — and neither has a Stripe session, which is     why &#x60;stripeCheckoutSessionId&#x60; is nullable.  A debit additionally carries the hour it bills for and the meter reading it came from, so the ledger can be checked against the usage events rather than taken on trust. One table rather than two because the balance has to be the sum of money in and money out, and a second table would make every balance read a join.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**creditTransactionsGet()**](CreditTransactionApi.md#creditTransactionsGet) | **GET** /api/credit_transactions/{id} | Retrieves a CreditTransaction resource. |
| [**creditTransactionsList()**](CreditTransactionApi.md#creditTransactionsList) | **GET** /api/credit_transactions | Retrieves the collection of CreditTransaction resources. |


## `creditTransactionsGet()`

```php
creditTransactionsGet($id): \SomeonesComputer\Sdk\Model\CreditTransaction
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
    $result = $apiInstance->creditTransactionsGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditTransactionApi->creditTransactionsGet: ', $e->getMessage(), PHP_EOL;
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

## `creditTransactionsList()`

```php
creditTransactionsList($page): \SomeonesComputer\Sdk\Model\CreditTransaction[]
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
    $result = $apiInstance->creditTransactionsList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditTransactionApi->creditTransactionsList: ', $e->getMessage(), PHP_EOL;
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
