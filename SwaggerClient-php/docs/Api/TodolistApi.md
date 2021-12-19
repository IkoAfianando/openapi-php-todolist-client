# Swagger\Client\TodolistApi

All URIs are relative to *https://{environment}.programmingwithiko.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**todolistGet**](TodolistApi.md#todolistget) | **GET** /todolist | Get All Todolist
[**todolistPost**](TodolistApi.md#todolistpost) | **POST** /todolist | Create New Todolist
[**todollistTodolistIdDelete**](TodolistApi.md#todollisttodolistiddelete) | **DELETE** /todollist/{todolistId} | Delete existing Todolist
[**todollistTodolistIdPut**](TodolistApi.md#todollisttodolistidput) | **PUT** /todollist/{todolistId} | Update existing Todolist

# **todolistGet**
> \Swagger\Client\Model\ArrayTodolist todolistGet($include_done, $name)

Get All Todolist

Get all todolist by default

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include_done = false; // bool | Include done todolist in the result
$name = "name_example"; // string | Filter todolist by name

try {
    $result = $apiInstance->todolistGet($include_done, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **include_done** | **bool**| Include done todolist in the result | [optional] [default to false]
 **name** | **string**| Filter todolist by name | [optional]

### Return type

[**\Swagger\Client\Model\ArrayTodolist**](../Model/ArrayTodolist.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todolistPost**
> \Swagger\Client\Model\Todolist todolistPost($body)

Create New Todolist

Create new todolist to database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CreateOrUpdateTodolist(); // \Swagger\Client\Model\CreateOrUpdateTodolist | 

try {
    $result = $apiInstance->todolistPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todolistPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CreateOrUpdateTodolist**](../Model/CreateOrUpdateTodolist.md)|  |

### Return type

[**\Swagger\Client\Model\Todolist**](../Model/Todolist.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todollistTodolistIdDelete**
> \Swagger\Client\Model\InlineResponse200 todollistTodolistIdDelete($todolist_id)

Delete existing Todolist

Delete existing todolist in database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$todolist_id = "todolist_id_example"; // string | Todolist id for updated

try {
    $result = $apiInstance->todollistTodolistIdDelete($todolist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todollistTodolistIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **todolist_id** | **string**| Todolist id for updated |

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **todollistTodolistIdPut**
> \Swagger\Client\Model\Todolist todollistTodolistIdPut($body, $todolist_id)

Update existing Todolist

Update existing todolist in database

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: TodolistAuth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\TodolistApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CreateOrUpdateTodolist(); // \Swagger\Client\Model\CreateOrUpdateTodolist | 
$todolist_id = "todolist_id_example"; // string | Todolist id for updated

try {
    $result = $apiInstance->todollistTodolistIdPut($body, $todolist_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodolistApi->todollistTodolistIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CreateOrUpdateTodolist**](../Model/CreateOrUpdateTodolist.md)|  |
 **todolist_id** | **string**| Todolist id for updated |

### Return type

[**\Swagger\Client\Model\Todolist**](../Model/Todolist.md)

### Authorization

[TodolistAuth](../../README.md#TodolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

