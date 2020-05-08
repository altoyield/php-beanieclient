# Swagger\Client\WorkCentreGroupApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**findWorkCentreGroupById**](WorkCentreGroupApi.md#findWorkCentreGroupById) | **GET** /work_centre_groups/{id} | Find Work centre group by ID
[**findWorkCentreGroups**](WorkCentreGroupApi.md#findWorkCentreGroups) | **GET** /work_centre_groups | All work centre group


# **findWorkCentreGroupById**
> \Swagger\Client\Model\WorkCentreGroup findWorkCentreGroupById($id)

Find Work centre group by ID

Returns a single work centre group if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\WorkCentreGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of work centre group to fetch

try {
    $result = $apiInstance->findWorkCentreGroupById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkCentreGroupApi->findWorkCentreGroupById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of work centre group to fetch |

### Return type

[**\Swagger\Client\Model\WorkCentreGroup**](../Model/WorkCentreGroup.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findWorkCentreGroups**
> \Swagger\Client\Model\WorkCentreGroup[] findWorkCentreGroups($tags, $limit)

All work centre group

Returns all work centre group from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\WorkCentreGroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findWorkCentreGroups($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkCentreGroupApi->findWorkCentreGroups: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\WorkCentreGroup[]**](../Model/WorkCentreGroup.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

