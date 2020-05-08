# Swagger\Client\NominalAccountCategoryApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addNominalAccountCategory**](NominalAccountCategoryApi.md#addNominalAccountCategory) | **POST** /nominal_account_categories | 
[**findNominalAccountCategories**](NominalAccountCategoryApi.md#findNominalAccountCategories) | **GET** /nominal_account_categories | All nominal account category
[**findNominalAccountCategoryById**](NominalAccountCategoryApi.md#findNominalAccountCategoryById) | **GET** /nominal_account_categories/{id} | Find Nominal account category by ID


# **addNominalAccountCategory**
> \Swagger\Client\Model\NominalAccountCategory addNominalAccountCategory($nominal_account_categories)



Creates a new nominal account category in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountCategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$nominal_account_categories = new \Swagger\Client\Model\NominalAccountCategoryInput(); // \Swagger\Client\Model\NominalAccountCategoryInput | Nominal account category to add to the system

try {
    $result = $apiInstance->addNominalAccountCategory($nominal_account_categories);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountCategoryApi->addNominalAccountCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nominal_account_categories** | [**\Swagger\Client\Model\NominalAccountCategoryInput**](../Model/NominalAccountCategoryInput.md)| Nominal account category to add to the system |

### Return type

[**\Swagger\Client\Model\NominalAccountCategory**](../Model/NominalAccountCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findNominalAccountCategories**
> \Swagger\Client\Model\NominalAccountCategory[] findNominalAccountCategories($tags, $limit)

All nominal account category

Returns all nominal account category from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountCategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findNominalAccountCategories($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountCategoryApi->findNominalAccountCategories: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\NominalAccountCategory[]**](../Model/NominalAccountCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findNominalAccountCategoryById**
> \Swagger\Client\Model\NominalAccountCategory findNominalAccountCategoryById($id)

Find Nominal account category by ID

Returns a single nominal account category if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountCategoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of nominal account category to fetch

try {
    $result = $apiInstance->findNominalAccountCategoryById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountCategoryApi->findNominalAccountCategoryById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of nominal account category to fetch |

### Return type

[**\Swagger\Client\Model\NominalAccountCategory**](../Model/NominalAccountCategory.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

