# Swagger\Client\WorkCentreApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**findWorkCentreById**](WorkCentreApi.md#findWorkCentreById) | **GET** /work_centres/{id} | Find Work centre by ID
[**findWorkCentres**](WorkCentreApi.md#findWorkCentres) | **GET** /work_centre_groups/{work_centre_group_id}/work_centres | All work centre


# **findWorkCentreById**
> \Swagger\Client\Model\WorkCentre findWorkCentreById($id)

Find Work centre by ID

Returns a single work centre if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\WorkCentreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of work centre to fetch

try {
    $result = $apiInstance->findWorkCentreById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkCentreApi->findWorkCentreById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of work centre to fetch |

### Return type

[**\Swagger\Client\Model\WorkCentre**](../Model/WorkCentre.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findWorkCentres**
> \Swagger\Client\Model\WorkCentre[] findWorkCentres($work_centre_group_id, $tags, $limit)

All work centre

Returns all work centre from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\WorkCentreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$work_centre_group_id = 789; // int | ID of Work Centre Group for list of Work Centres
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findWorkCentres($work_centre_group_id, $tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkCentreApi->findWorkCentres: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **work_centre_group_id** | **int**| ID of Work Centre Group for list of Work Centres |
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\WorkCentre[]**](../Model/WorkCentre.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

