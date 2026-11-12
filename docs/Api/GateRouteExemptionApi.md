# SomeonesComputer\Sdk\GateRouteExemptionApi

An owner or admin&#39;s approval of one route that compose declared as exempt from the access gate (&#x60;x-someones.gate_exempt&#x60;, {@see GateExemption}).  **The compose file asks and this row grants.** {@see \\App\\Service\\Ingress\\IngressPlanner} writes the exempt router only for a declaration that matches a row here on every field: service, host, path prefix and methods. A redeploy that changes any of them leaves the old row matching nothing, so the new declaration is pending again and the old route closes at once.  Only approvals have rows. \&quot;Pending\&quot; is a declaration with no matching row, the same shape as {@see AdoptionApproval}.  The operations show in the OpenAPI document and in the four generated SDKs.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiGateRouteExemptionsGetCollection()**](GateRouteExemptionApi.md#apiGateRouteExemptionsGetCollection) | **GET** /api/gate_route_exemptions | Retrieves the collection of GateRouteExemption resources. |
| [**apiGateRouteExemptionsIdDelete()**](GateRouteExemptionApi.md#apiGateRouteExemptionsIdDelete) | **DELETE** /api/gate_route_exemptions/{id} | Removes the GateRouteExemption resource. |
| [**apiGateRouteExemptionsIdGet()**](GateRouteExemptionApi.md#apiGateRouteExemptionsIdGet) | **GET** /api/gate_route_exemptions/{id} | Retrieves a GateRouteExemption resource. |
| [**apiGateRouteExemptionsPost()**](GateRouteExemptionApi.md#apiGateRouteExemptionsPost) | **POST** /api/gate_route_exemptions | Creates a GateRouteExemption resource. |


## `apiGateRouteExemptionsGetCollection()`

```php
apiGateRouteExemptionsGetCollection($page): \SomeonesComputer\Sdk\Model\GateRouteExemption[]
```

Retrieves the collection of GateRouteExemption resources.

Retrieves the collection of GateRouteExemption resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GateRouteExemptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiGateRouteExemptionsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GateRouteExemptionApi->apiGateRouteExemptionsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\GateRouteExemption[]**](../Model/GateRouteExemption.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiGateRouteExemptionsIdDelete()`

```php
apiGateRouteExemptionsIdDelete($id)
```

Removes the GateRouteExemption resource.

Removes the GateRouteExemption resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GateRouteExemptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GateRouteExemption identifier

try {
    $apiInstance->apiGateRouteExemptionsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling GateRouteExemptionApi->apiGateRouteExemptionsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GateRouteExemption identifier | |

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

## `apiGateRouteExemptionsIdGet()`

```php
apiGateRouteExemptionsIdGet($id): \SomeonesComputer\Sdk\Model\GateRouteExemption
```

Retrieves a GateRouteExemption resource.

Retrieves a GateRouteExemption resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GateRouteExemptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GateRouteExemption identifier

try {
    $result = $apiInstance->apiGateRouteExemptionsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GateRouteExemptionApi->apiGateRouteExemptionsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GateRouteExemption identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\GateRouteExemption**](../Model/GateRouteExemption.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiGateRouteExemptionsPost()`

```php
apiGateRouteExemptionsPost($gate_route_exemption_gate_route_exemption_input): \SomeonesComputer\Sdk\Model\GateRouteExemption
```

Creates a GateRouteExemption resource.

Creates a GateRouteExemption resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GateRouteExemptionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gate_route_exemption_gate_route_exemption_input = new \SomeonesComputer\Sdk\Model\GateRouteExemptionGateRouteExemptionInput(); // \SomeonesComputer\Sdk\Model\GateRouteExemptionGateRouteExemptionInput | The new GateRouteExemption resource

try {
    $result = $apiInstance->apiGateRouteExemptionsPost($gate_route_exemption_gate_route_exemption_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GateRouteExemptionApi->apiGateRouteExemptionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gate_route_exemption_gate_route_exemption_input** | [**\SomeonesComputer\Sdk\Model\GateRouteExemptionGateRouteExemptionInput**](../Model/GateRouteExemptionGateRouteExemptionInput.md)| The new GateRouteExemption resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\GateRouteExemption**](../Model/GateRouteExemption.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
