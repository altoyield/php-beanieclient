# Swagger\Client\ProductionOrderApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addProductionOrder**](ProductionOrderApi.md#addProductionOrder) | **POST** /production_orders | 
[**findProductionOrderById**](ProductionOrderApi.md#findProductionOrderById) | **GET** /production_orders/{id} | Find Production order by ID
[**findProductionOrders**](ProductionOrderApi.md#findProductionOrders) | **GET** /production_orders | All production order


# **addProductionOrder**
> \Swagger\Client\Model\ProductionOrder addProductionOrder($production_orders)



Creates a new production order in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_orders = new \Swagger\Client\Model\ProductionOrderInput(); // \Swagger\Client\Model\ProductionOrderInput | Production order to add to the system

try {
    $result = $apiInstance->addProductionOrder($production_orders);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->addProductionOrder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_orders** | [**\Swagger\Client\Model\ProductionOrderInput**](../Model/ProductionOrderInput.md)| Production order to add to the system |

### Return type

[**\Swagger\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findProductionOrderById**
> \Swagger\Client\Model\ProductionOrder findProductionOrderById($id)

Find Production order by ID

Returns a single production order if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of production order to fetch

try {
    $result = $apiInstance->findProductionOrderById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->findProductionOrderById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of production order to fetch |

### Return type

[**\Swagger\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findProductionOrders**
> \Swagger\Client\Model\ProductionOrder[] findProductionOrders($tags, $limit)

All production order

Returns all production order from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findProductionOrders($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->findProductionOrders: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\ProductionOrder[]**](../Model/ProductionOrder.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

