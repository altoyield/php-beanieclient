# Swagger\Client\StockSupplierApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addStockSupplier**](StockSupplierApi.md#addStockSupplier) | **POST** /stock_suppliers | 
[**findStockSupplierById**](StockSupplierApi.md#findStockSupplierById) | **GET** /stock_suppliers/{id} | Find Stock supplier by ID
[**findStockSuppliers**](StockSupplierApi.md#findStockSuppliers) | **GET** /stock_suppliers | All stock supplier


# **addStockSupplier**
> \Swagger\Client\Model\StockSupplier addStockSupplier($stock_suppliers)



Creates a new stock supplier in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockSupplierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_suppliers = new \Swagger\Client\Model\StockSupplierInput(); // \Swagger\Client\Model\StockSupplierInput | Stock supplier to add to the system

try {
    $result = $apiInstance->addStockSupplier($stock_suppliers);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockSupplierApi->addStockSupplier: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_suppliers** | [**\Swagger\Client\Model\StockSupplierInput**](../Model/StockSupplierInput.md)| Stock supplier to add to the system |

### Return type

[**\Swagger\Client\Model\StockSupplier**](../Model/StockSupplier.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findStockSupplierById**
> \Swagger\Client\Model\StockSupplier findStockSupplierById($id)

Find Stock supplier by ID

Returns a single stock supplier if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockSupplierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of stock supplier to fetch

try {
    $result = $apiInstance->findStockSupplierById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockSupplierApi->findStockSupplierById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of stock supplier to fetch |

### Return type

[**\Swagger\Client\Model\StockSupplier**](../Model/StockSupplier.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findStockSuppliers**
> \Swagger\Client\Model\StockSupplier[] findStockSuppliers($tags, $limit)

All stock supplier

Returns all stock supplier from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\StockSupplierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findStockSuppliers($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockSupplierApi->findStockSuppliers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\StockSupplier[]**](../Model/StockSupplier.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

