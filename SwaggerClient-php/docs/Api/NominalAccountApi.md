# Swagger\Client\NominalAccountApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addNominalAccount**](NominalAccountApi.md#addNominalAccount) | **POST** /nominal_accounts | 
[**findNominalAccountById**](NominalAccountApi.md#findNominalAccountById) | **GET** /nominal_accounts/{id} | Find Nominal account by ID
[**findNominalAccounts**](NominalAccountApi.md#findNominalAccounts) | **GET** /nominal_accounts | All nominal account


# **addNominalAccount**
> \Swagger\Client\Model\NominalAccount addNominalAccount($nominal_accounts)



Creates a new nominal account in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$nominal_accounts = new \Swagger\Client\Model\NominalAccountInput(); // \Swagger\Client\Model\NominalAccountInput | Nominal account to add to the system

try {
    $result = $apiInstance->addNominalAccount($nominal_accounts);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountApi->addNominalAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nominal_accounts** | [**\Swagger\Client\Model\NominalAccountInput**](../Model/NominalAccountInput.md)| Nominal account to add to the system |

### Return type

[**\Swagger\Client\Model\NominalAccount**](../Model/NominalAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findNominalAccountById**
> \Swagger\Client\Model\NominalAccount findNominalAccountById($id)

Find Nominal account by ID

Returns a single nominal account if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of nominal account to fetch

try {
    $result = $apiInstance->findNominalAccountById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountApi->findNominalAccountById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of nominal account to fetch |

### Return type

[**\Swagger\Client\Model\NominalAccount**](../Model/NominalAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findNominalAccounts**
> \Swagger\Client\Model\NominalAccount[] findNominalAccounts($tags, $limit)

All nominal account

Returns all nominal account from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NominalAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findNominalAccounts($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NominalAccountApi->findNominalAccounts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\NominalAccount[]**](../Model/NominalAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

