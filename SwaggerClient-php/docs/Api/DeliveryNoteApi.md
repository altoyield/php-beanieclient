# Swagger\Client\DeliveryNoteApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addDeliveryNote**](DeliveryNoteApi.md#addDeliveryNote) | **POST** /delivery_notes | 
[**findDeliveryNoteById**](DeliveryNoteApi.md#findDeliveryNoteById) | **GET** /delivery_notes/{id} | Find Delivery note by ID
[**findDeliveryNotes**](DeliveryNoteApi.md#findDeliveryNotes) | **GET** /delivery_notes | All delivery note


# **addDeliveryNote**
> \Swagger\Client\Model\DeliveryNote addDeliveryNote($delivery_notes)



Creates a new delivery note in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeliveryNoteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_notes = new \Swagger\Client\Model\DeliveryNoteInput(); // \Swagger\Client\Model\DeliveryNoteInput | Delivery note to add to the system

try {
    $result = $apiInstance->addDeliveryNote($delivery_notes);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryNoteApi->addDeliveryNote: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_notes** | [**\Swagger\Client\Model\DeliveryNoteInput**](../Model/DeliveryNoteInput.md)| Delivery note to add to the system |

### Return type

[**\Swagger\Client\Model\DeliveryNote**](../Model/DeliveryNote.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findDeliveryNoteById**
> \Swagger\Client\Model\DeliveryNote findDeliveryNoteById($id)

Find Delivery note by ID

Returns a single delivery note if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeliveryNoteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of delivery note to fetch

try {
    $result = $apiInstance->findDeliveryNoteById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryNoteApi->findDeliveryNoteById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of delivery note to fetch |

### Return type

[**\Swagger\Client\Model\DeliveryNote**](../Model/DeliveryNote.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findDeliveryNotes**
> \Swagger\Client\Model\DeliveryNote[] findDeliveryNotes($tags, $limit)

All delivery note

Returns all delivery note from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DeliveryNoteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findDeliveryNotes($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryNoteApi->findDeliveryNotes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\DeliveryNote[]**](../Model/DeliveryNote.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

