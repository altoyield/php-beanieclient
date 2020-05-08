# Swagger\Client\PurchaseInvoiceApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPurchaseInvoice**](PurchaseInvoiceApi.md#addPurchaseInvoice) | **POST** /purchase_invoices | 
[**findPurchaseInvoiceById**](PurchaseInvoiceApi.md#findPurchaseInvoiceById) | **GET** /purchase_invoices/{id} | Find Purchase invoice by ID
[**findPurchaseInvoices**](PurchaseInvoiceApi.md#findPurchaseInvoices) | **GET** /purchase_invoices | All purchase invoice


# **addPurchaseInvoice**
> \Swagger\Client\Model\PurchaseInvoice addPurchaseInvoice($purchase_invoices)



Creates a new purchase invoice in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_invoices = new \Swagger\Client\Model\PurchaseInvoiceInput(); // \Swagger\Client\Model\PurchaseInvoiceInput | Purchase invoice to add to the system

try {
    $result = $apiInstance->addPurchaseInvoice($purchase_invoices);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->addPurchaseInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_invoices** | [**\Swagger\Client\Model\PurchaseInvoiceInput**](../Model/PurchaseInvoiceInput.md)| Purchase invoice to add to the system |

### Return type

[**\Swagger\Client\Model\PurchaseInvoice**](../Model/PurchaseInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findPurchaseInvoiceById**
> \Swagger\Client\Model\PurchaseInvoice findPurchaseInvoiceById($id)

Find Purchase invoice by ID

Returns a single purchase invoice if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of purchase invoice to fetch

try {
    $result = $apiInstance->findPurchaseInvoiceById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->findPurchaseInvoiceById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of purchase invoice to fetch |

### Return type

[**\Swagger\Client\Model\PurchaseInvoice**](../Model/PurchaseInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findPurchaseInvoices**
> \Swagger\Client\Model\PurchaseInvoice[] findPurchaseInvoices($tags, $limit)

All purchase invoice

Returns all purchase invoice from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findPurchaseInvoices($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->findPurchaseInvoices: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\PurchaseInvoice[]**](../Model/PurchaseInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

