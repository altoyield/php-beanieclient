# Swagger\Client\PartnerAddressApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPartnerAddress**](PartnerAddressApi.md#addPartnerAddress) | **POST** /partner_addresses | 
[**findPartnerAddressById**](PartnerAddressApi.md#findPartnerAddressById) | **GET** /partner_addresses/{id} | Find Partner address by ID
[**findPartnerAddresses**](PartnerAddressApi.md#findPartnerAddresses) | **GET** /partner_addresses | All partner address


# **addPartnerAddress**
> \Swagger\Client\Model\PartnerAddress addPartnerAddress($partner_addresses)



Creates a new partner address in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PartnerAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$partner_addresses = new \Swagger\Client\Model\PartnerAddressInput(); // \Swagger\Client\Model\PartnerAddressInput | Partner address to add to the system

try {
    $result = $apiInstance->addPartnerAddress($partner_addresses);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerAddressApi->addPartnerAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **partner_addresses** | [**\Swagger\Client\Model\PartnerAddressInput**](../Model/PartnerAddressInput.md)| Partner address to add to the system |

### Return type

[**\Swagger\Client\Model\PartnerAddress**](../Model/PartnerAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findPartnerAddressById**
> \Swagger\Client\Model\PartnerAddress findPartnerAddressById($id)

Find Partner address by ID

Returns a single partner address if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PartnerAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of partner address to fetch

try {
    $result = $apiInstance->findPartnerAddressById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerAddressApi->findPartnerAddressById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of partner address to fetch |

### Return type

[**\Swagger\Client\Model\PartnerAddress**](../Model/PartnerAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findPartnerAddresses**
> \Swagger\Client\Model\PartnerAddress[] findPartnerAddresses($tags, $limit)

All partner address

Returns all partner address from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\PartnerAddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findPartnerAddresses($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerAddressApi->findPartnerAddresses: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\PartnerAddress[]**](../Model/PartnerAddress.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

