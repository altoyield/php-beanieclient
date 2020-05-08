# Swagger\Client\FixedAssetApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addFixedAsset**](FixedAssetApi.md#addFixedAsset) | **POST** /fixed_assets | 
[**findFixedAssetById**](FixedAssetApi.md#findFixedAssetById) | **GET** /fixed_assets/{id} | Find Fixed asset by ID
[**findFixedAssets**](FixedAssetApi.md#findFixedAssets) | **GET** /fixed_assets | All fixed asset


# **addFixedAsset**
> \Swagger\Client\Model\FixedAsset addFixedAsset($fixed_assets)



Creates a new fixed asset in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\FixedAssetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fixed_assets = new \Swagger\Client\Model\FixedAssetInput(); // \Swagger\Client\Model\FixedAssetInput | Fixed asset to add to the system

try {
    $result = $apiInstance->addFixedAsset($fixed_assets);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FixedAssetApi->addFixedAsset: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fixed_assets** | [**\Swagger\Client\Model\FixedAssetInput**](../Model/FixedAssetInput.md)| Fixed asset to add to the system |

### Return type

[**\Swagger\Client\Model\FixedAsset**](../Model/FixedAsset.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findFixedAssetById**
> \Swagger\Client\Model\FixedAsset findFixedAssetById($id)

Find Fixed asset by ID

Returns a single fixed asset if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\FixedAssetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of fixed asset to fetch

try {
    $result = $apiInstance->findFixedAssetById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FixedAssetApi->findFixedAssetById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of fixed asset to fetch |

### Return type

[**\Swagger\Client\Model\FixedAsset**](../Model/FixedAsset.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findFixedAssets**
> \Swagger\Client\Model\FixedAsset[] findFixedAssets($tags, $limit)

All fixed asset

Returns all fixed asset from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\FixedAssetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findFixedAssets($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FixedAssetApi->findFixedAssets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\FixedAsset[]**](../Model/FixedAsset.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

