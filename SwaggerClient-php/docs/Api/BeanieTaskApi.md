# Swagger\Client\BeanieTaskApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addBeanieTask**](BeanieTaskApi.md#addBeanieTask) | **POST** /beanie_tasks | 
[**findBeanieTaskById**](BeanieTaskApi.md#findBeanieTaskById) | **GET** /beanie_tasks/{id} | Find Beanie task by ID
[**findBeanieTasks**](BeanieTaskApi.md#findBeanieTasks) | **GET** /beanie_tasks | All beanie task


# **addBeanieTask**
> \Swagger\Client\Model\BeanieTask addBeanieTask($beanie_tasks)



Creates a new beanie task in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BeanieTaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$beanie_tasks = new \Swagger\Client\Model\BeanieTaskInput(); // \Swagger\Client\Model\BeanieTaskInput | Beanie task to add to the system

try {
    $result = $apiInstance->addBeanieTask($beanie_tasks);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BeanieTaskApi->addBeanieTask: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **beanie_tasks** | [**\Swagger\Client\Model\BeanieTaskInput**](../Model/BeanieTaskInput.md)| Beanie task to add to the system |

### Return type

[**\Swagger\Client\Model\BeanieTask**](../Model/BeanieTask.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBeanieTaskById**
> \Swagger\Client\Model\BeanieTask findBeanieTaskById($id)

Find Beanie task by ID

Returns a single beanie task if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BeanieTaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of beanie task to fetch

try {
    $result = $apiInstance->findBeanieTaskById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BeanieTaskApi->findBeanieTaskById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of beanie task to fetch |

### Return type

[**\Swagger\Client\Model\BeanieTask**](../Model/BeanieTask.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBeanieTasks**
> \Swagger\Client\Model\BeanieTask[] findBeanieTasks($tags, $limit)

All beanie task

Returns all beanie task from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BeanieTaskApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findBeanieTasks($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BeanieTaskApi->findBeanieTasks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\BeanieTask[]**](../Model/BeanieTask.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

