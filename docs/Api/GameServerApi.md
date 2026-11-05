# SomeonesComputer\Sdk\GameServerApi

A managed game server: a game image that runs on the platform, with a volume that keeps its world.

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gameServersCreate()**](GameServerApi.md#gameServersCreate) | **POST** /api/game_servers | Creates a GameServer resource. |
| [**gameServersDelete()**](GameServerApi.md#gameServersDelete) | **DELETE** /api/game_servers/{id} | Removes the GameServer resource. |
| [**gameServersGet()**](GameServerApi.md#gameServersGet) | **GET** /api/game_servers/{id} | Retrieves a GameServer resource. |
| [**gameServersList()**](GameServerApi.md#gameServersList) | **GET** /api/game_servers | Retrieves the collection of GameServer resources. |
| [**gameServersRestart()**](GameServerApi.md#gameServersRestart) | **POST** /api/game_servers/{id}/restart | Creates a GameServer resource. |
| [**gameServersStart()**](GameServerApi.md#gameServersStart) | **POST** /api/game_servers/{id}/start | Creates a GameServer resource. |
| [**gameServersStop()**](GameServerApi.md#gameServersStop) | **POST** /api/game_servers/{id}/stop | Creates a GameServer resource. |
| [**gameServersUpdate()**](GameServerApi.md#gameServersUpdate) | **PATCH** /api/game_servers/{id} | Updates the GameServer resource. |


## `gameServersCreate()`

```php
gameServersCreate($game_server_game_server_input): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Creates a GameServer resource.

Creates a GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$game_server_game_server_input = new \SomeonesComputer\Sdk\Model\GameServerGameServerInput(); // \SomeonesComputer\Sdk\Model\GameServerGameServerInput | The new GameServer resource

try {
    $result = $apiInstance->gameServersCreate($game_server_game_server_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **game_server_game_server_input** | [**\SomeonesComputer\Sdk\Model\GameServerGameServerInput**](../Model/GameServerGameServerInput.md)| The new GameServer resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersDelete()`

```php
gameServersDelete($id)
```

Removes the GameServer resource.

Removes the GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier

try {
    $apiInstance->gameServersDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |

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

## `gameServersGet()`

```php
gameServersGet($id): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Retrieves a GameServer resource.

Retrieves a GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier

try {
    $result = $apiInstance->gameServersGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersList()`

```php
gameServersList($page): \SomeonesComputer\Sdk\Model\GameServerGameServerRead[]
```

Retrieves the collection of GameServer resources.

Retrieves the collection of GameServer resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->gameServersList($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| The collection page number | [optional] [default to 1] |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead[]**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersRestart()`

```php
gameServersRestart($id): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Creates a GameServer resource.

Creates a GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier

try {
    $result = $apiInstance->gameServersRestart($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersRestart: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersStart()`

```php
gameServersStart($id): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Creates a GameServer resource.

Creates a GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier

try {
    $result = $apiInstance->gameServersStart($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersStart: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersStop()`

```php
gameServersStop($id): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Creates a GameServer resource.

Creates a GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier

try {
    $result = $apiInstance->gameServersStop($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersStop: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `gameServersUpdate()`

```php
gameServersUpdate($id, $game_server_game_server_settings_input_json_merge_patch): \SomeonesComputer\Sdk\Model\GameServerGameServerRead
```

Updates the GameServer resource.

Updates the GameServer resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\GameServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | GameServer identifier
$game_server_game_server_settings_input_json_merge_patch = new \SomeonesComputer\Sdk\Model\GameServerGameServerSettingsInputJsonMergePatch(); // \SomeonesComputer\Sdk\Model\GameServerGameServerSettingsInputJsonMergePatch | The updated GameServer resource

try {
    $result = $apiInstance->gameServersUpdate($id, $game_server_game_server_settings_input_json_merge_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GameServerApi->gameServersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| GameServer identifier | |
| **game_server_game_server_settings_input_json_merge_patch** | [**\SomeonesComputer\Sdk\Model\GameServerGameServerSettingsInputJsonMergePatch**](../Model/GameServerGameServerSettingsInputJsonMergePatch.md)| The updated GameServer resource | |

### Return type

[**\SomeonesComputer\Sdk\Model\GameServerGameServerRead**](../Model/GameServerGameServerRead.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
