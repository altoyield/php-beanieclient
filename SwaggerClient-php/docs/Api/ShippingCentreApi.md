# Swagger\Client\ShippingCentreApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addShippingCentre**](ShippingCentreApi.md#addShippingCentre) | **POST** /shipping_centres | 
[**findShippingCentreById**](ShippingCentreApi.md#findShippingCentreById) | **GET** /shipping_centres/{id} | Find Shipping centre by ID
[**findShippingCentres**](ShippingCentreApi.md#findShippingCentres) | **GET** /shipping_centres | All shipping centre


# **addShippingCentre**
> \Swagger\Client\Model\ShippingCentre addShippingCentre($shipping_centres)



Creates a new shipping centre in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ShippingCentreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipping_centres = new \Swagger\Client\Model\ShippingCentreInput(); // \Swagger\Client\Model\ShippingCentreInput | Shipping centre to add to the system

try {
    $result = $apiInstance->addShippingCentre($shipping_centres);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingCentreApi->addShippingCentre: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipping_centres** | [**\Swagger\Client\Model\ShippingCentreInput**](../Model/ShippingCentreInput.md)| Shipping centre to add to the system |

### Return type

[**\Swagger\Client\Model\ShippingCentre**](../Model/ShippingCentre.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findShippingCentreById**
> \Swagger\Client\Model\ShippingCentre findShippingCentreById($id)

Find Shipping centre by ID

Returns a single shipping centre if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ShippingCentreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of shipping centre to fetch

try {
    $result = $apiInstance->findShippingCentreById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingCentreApi->findShippingCentreById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of shipping centre to fetch |

### Return type

[**\Swagger\Client\Model\ShippingCentre**](../Model/ShippingCentre.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findShippingCentres**
> \Swagger\Client\Model\ShippingCentre[] findShippingCentres($tags, $limit)

All shipping centre

Returns all shipping centre from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ShippingCentreApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findShippingCentres($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingCentreApi->findShippingCentres: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\ShippingCentre[]**](../Model/ShippingCentre.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

