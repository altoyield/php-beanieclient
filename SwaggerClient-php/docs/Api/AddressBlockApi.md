# Swagger\Client\AddressBlockApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addAddressBlock**](AddressBlockApi.md#addAddressBlock) | **POST** /address_blocks | 
[**findAddressBlockById**](AddressBlockApi.md#findAddressBlockById) | **GET** /address_blocks/{id} | Find Address block by ID
[**findAddressBlocks**](AddressBlockApi.md#findAddressBlocks) | **GET** /address_blocks | All address block


# **addAddressBlock**
> \Swagger\Client\Model\AddressBlock addAddressBlock($address_blocks)



Creates a new address block in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AddressBlockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$address_blocks = new \Swagger\Client\Model\AddressBlockInput(); // \Swagger\Client\Model\AddressBlockInput | Address block to add to the system

try {
    $result = $apiInstance->addAddressBlock($address_blocks);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBlockApi->addAddressBlock: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address_blocks** | [**\Swagger\Client\Model\AddressBlockInput**](../Model/AddressBlockInput.md)| Address block to add to the system |

### Return type

[**\Swagger\Client\Model\AddressBlock**](../Model/AddressBlock.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAddressBlockById**
> \Swagger\Client\Model\AddressBlock findAddressBlockById($id)

Find Address block by ID

Returns a single address block if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AddressBlockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of address block to fetch

try {
    $result = $apiInstance->findAddressBlockById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBlockApi->findAddressBlockById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of address block to fetch |

### Return type

[**\Swagger\Client\Model\AddressBlock**](../Model/AddressBlock.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAddressBlocks**
> \Swagger\Client\Model\AddressBlock[] findAddressBlocks($tags, $limit)

All address block

Returns all address block from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AddressBlockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findAddressBlocks($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressBlockApi->findAddressBlocks: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\AddressBlock[]**](../Model/AddressBlock.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

