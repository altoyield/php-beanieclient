# Swagger\Client\BillableApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addBillable**](BillableApi.md#addBillable) | **POST** /billables | 
[**findBillableById**](BillableApi.md#findBillableById) | **GET** /billables/{id} | Find Billable record by ID
[**findBillables**](BillableApi.md#findBillables) | **GET** /billables | All billable record


# **addBillable**
> \Swagger\Client\Model\Billable addBillable($billables)



Creates a new billable record in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillableApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billables = new \Swagger\Client\Model\BillableInput(); // \Swagger\Client\Model\BillableInput | Billable record to add to the system

try {
    $result = $apiInstance->addBillable($billables);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillableApi->addBillable: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **billables** | [**\Swagger\Client\Model\BillableInput**](../Model/BillableInput.md)| Billable record to add to the system |

### Return type

[**\Swagger\Client\Model\Billable**](../Model/Billable.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBillableById**
> \Swagger\Client\Model\Billable findBillableById($id)

Find Billable record by ID

Returns a single billable record if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillableApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of billable record to fetch

try {
    $result = $apiInstance->findBillableById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillableApi->findBillableById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of billable record to fetch |

### Return type

[**\Swagger\Client\Model\Billable**](../Model/Billable.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBillables**
> \Swagger\Client\Model\Billable[] findBillables($tags, $limit)

All billable record

Returns all billable record from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillableApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findBillables($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillableApi->findBillables: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\Billable[]**](../Model/Billable.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

