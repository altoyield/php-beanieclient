# Swagger\Client\BankAccountApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addBankAccount**](BankAccountApi.md#addBankAccount) | **POST** /bank_accounts | 
[**findBankAccountById**](BankAccountApi.md#findBankAccountById) | **GET** /bank_accounts/{id} | Find Bank Account by ID
[**findBankAccounts**](BankAccountApi.md#findBankAccounts) | **GET** /bank_accounts | All bank accounts


# **addBankAccount**
> \Swagger\Client\Model\BankAccount addBankAccount($bank_account)



Creates a new bank account in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bank_account = new \Swagger\Client\Model\BankAccountInput(); // \Swagger\Client\Model\BankAccountInput | Bank account to add to the system

try {
    $result = $apiInstance->addBankAccount($bank_account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->addBankAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bank_account** | [**\Swagger\Client\Model\BankAccountInput**](../Model/BankAccountInput.md)| Bank account to add to the system |

### Return type

[**\Swagger\Client\Model\BankAccount**](../Model/BankAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBankAccountById**
> \Swagger\Client\Model\BankAccount findBankAccountById($id)

Find Bank Account by ID

Returns a single bank account if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of bank account to fetch

try {
    $result = $apiInstance->findBankAccountById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->findBankAccountById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of bank account to fetch |

### Return type

[**\Swagger\Client\Model\BankAccount**](../Model/BankAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBankAccounts**
> \Swagger\Client\Model\BankAccount[] findBankAccounts($tags, $limit)

All bank accounts

Returns all bank accounts from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BankAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | maximum number of results to return

try {
    $result = $apiInstance->findBankAccounts($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankAccountApi->findBankAccounts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\BankAccount[]**](../Model/BankAccount.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

