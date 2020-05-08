# Swagger\Client\SalesInvoiceApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addSalesInvoice**](SalesInvoiceApi.md#addSalesInvoice) | **POST** /sales_invoices | 
[**findSalesInvoiceById**](SalesInvoiceApi.md#findSalesInvoiceById) | **GET** /sales_invoices/{id} | Find Sales invoice by ID
[**findSalesInvoices**](SalesInvoiceApi.md#findSalesInvoices) | **GET** /sales_invoices | All sales invoice


# **addSalesInvoice**
> \Swagger\Client\Model\SalesInvoice addSalesInvoice($sales_invoices)



Creates a new sales invoice in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sales_invoices = new \Swagger\Client\Model\SalesInvoiceInput(); // \Swagger\Client\Model\SalesInvoiceInput | Sales invoice to add to the system

try {
    $result = $apiInstance->addSalesInvoice($sales_invoices);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->addSalesInvoice: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sales_invoices** | [**\Swagger\Client\Model\SalesInvoiceInput**](../Model/SalesInvoiceInput.md)| Sales invoice to add to the system |

### Return type

[**\Swagger\Client\Model\SalesInvoice**](../Model/SalesInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findSalesInvoiceById**
> \Swagger\Client\Model\SalesInvoice findSalesInvoiceById($id)

Find Sales invoice by ID

Returns a single sales invoice if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of sales invoice to fetch

try {
    $result = $apiInstance->findSalesInvoiceById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->findSalesInvoiceById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of sales invoice to fetch |

### Return type

[**\Swagger\Client\Model\SalesInvoice**](../Model/SalesInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findSalesInvoices**
> \Swagger\Client\Model\SalesInvoice[] findSalesInvoices($tags, $limit)

All sales invoice

Returns all sales invoice from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findSalesInvoices($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->findSalesInvoices: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\SalesInvoice[]**](../Model/SalesInvoice.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

