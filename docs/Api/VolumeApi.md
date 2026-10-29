# SomeonesComputer\Sdk\VolumeApi

A named store of files that S3 holds, for a game server to keep its data in.  **A volume is a bucket with a name the tenant chose.** The bytes live in the {@see ManagedService} of kind Garage that this row owns. That reuses the quota, the metering, the credit gate and the retirement grace period that a bucket already has. It builds no second storage path. See docs/managed-game-servers.md.  The services list and &#x60;/managed_services&#x60; leave out the backing bucket ({@see \\App\\Repository\\ManagedServiceRepository::findForOrganization()} and {@see \\App\\ApiResource\\ManagedServiceOwnerExtension}). A tenant who retired it there would break the volume without a word.  Soft-deleted together with the bucket. Retiring a volume retires its bucket, so the data stays restorable for the grace period of {@see \\App\\Repository\\ManagedServiceRepository::GRACE_PERIOD}.  Unique per organization by slug, among live rows. A partial unique index in Version20261029101425&#39;s raw SQL does this, and the entity doesn&#39;t map it, for the reason {@see ManagedService} gives: DBAL drops the &#x60;WHERE&#x60; clause on SQLite. {@see VolumeRepository::findOneBySlug()} is the portable half of the rule.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**volumesCreate()**](VolumeApi.md#volumesCreate) | **POST** /api/volumes | Creates a Volume resource. |
| [**volumesDelete()**](VolumeApi.md#volumesDelete) | **DELETE** /api/volumes/{id} | Removes the Volume resource. |
| [**volumesGet()**](VolumeApi.md#volumesGet) | **GET** /api/volumes/{id} | Retrieves a Volume resource. |
| [**volumesList()**](VolumeApi.md#volumesList) | **GET** /api/volumes | Retrieves the collection of Volume resources. |


## `volumesCreate()`

```php
volumesCreate($volume_volume_input): \SomeonesComputer\Sdk\Model\Volume
```

Creates a Volume resource.

Creates a Volume resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\VolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$volume_volume_input = new \SomeonesComputer\Sdk\Model\VolumeVolumeInput(); // \SomeonesComputer\Sdk\Model\VolumeVolumeInput | The new Volume resource

try {
    $result = $apiInstance->volumesCreate($volume_volume_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VolumeApi->volumesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **volume_volume_input** | [**\SomeonesComputer\Sdk\Model\VolumeVolumeInput**](../Model/VolumeVolumeInput.md)| The new Volume resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\Volume**](../Model/Volume.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `volumesDelete()`

```php
volumesDelete($id)
```

Removes the Volume resource.

Removes the Volume resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\VolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Volume identifier

try {
    $apiInstance->volumesDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling VolumeApi->volumesDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Volume identifier | |

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

## `volumesGet()`

```php
volumesGet($id): \SomeonesComputer\Sdk\Model\Volume
```

Retrieves a Volume resource.

Retrieves a Volume resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\VolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | Volume identifier

try {
    $result = $apiInstance->volumesGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VolumeApi->volumesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Volume identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\Volume**](../Model/Volume.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `volumesList()`

```php
volumesList($page): \SomeonesComputer\Sdk\Model\Volume[]
```

Retrieves the collection of Volume resources.

Retrieves the collection of Volume resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\VolumeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->volumesList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VolumeApi->volumesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\Volume[]**](../Model/Volume.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
