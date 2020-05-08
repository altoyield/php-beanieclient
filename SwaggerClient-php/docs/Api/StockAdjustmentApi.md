# Swagger\Client\StockAdjustmentApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addStockAdjustment**](StockAdjustmentApi.md#addStockAdjustment) | **POST** /stock_adjustments | 
[**findStockAdjustmentById**](StockAdjustmentApi.md#findStockAdjustmentById) | **GET** /stock_adjustments/{id} | Find Stock adjustment by ID
[**findStockAdjustments**](StockAdjustmentApi.md#findStockAdjustments) | **GET** /stock_adjustments | All stock adjustment


# **addStockAdjustment**
> \Swagger\Client\Model\StockAdjustment addStockAdjustment($stock_adjustments)



Creates a new stock adjustment in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockAdjustmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_adjustments = new \Swagger\Client\Model\StockAdjustmentInput(); // \Swagger\Client\Model\StockAdjustmentInput | Stock adjustment to add to the system

try {
    $result = $apiInstance->addStockAdjustment($stock_adjustments);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockAdjustmentApi->addStockAdjustment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_adjustments** | [**\Swagger\Client\Model\StockAdjustmentInput**](../Model/StockAdjustmentInput.md)| Stock adjustment to add to the system |

### Return type

[**\Swagger\Client\Model\StockAdjustment**](../Model/StockAdjustment.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findStockAdjustmentById**
> \Swagger\Client\Model\StockAdjustment findStockAdjustmentById($id)

Find Stock adjustment by ID

Returns a single stock adjustment if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockAdjustmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of stock adjustment to fetch

try {
    $result = $apiInstance->findStockAdjustmentById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockAdjustmentApi->findStockAdjustmentById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of stock adjustment to fetch |

### Return type

[**\Swagger\Client\Model\StockAdjustment**](../Model/StockAdjustment.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findStockAdjustments**
> \Swagger\Client\Model\StockAdjustment[] findStockAdjustments($tags, $limit)

All stock adjustment

Returns all stock adjustment from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockAdjustmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findStockAdjustments($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockAdjustmentApi->findStockAdjustments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\StockAdjustment[]**](../Model/StockAdjustment.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

