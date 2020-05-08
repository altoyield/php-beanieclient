# Swagger\Client\JournalApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addJournal**](JournalApi.md#addJournal) | **POST** /journals | 
[**findJournalById**](JournalApi.md#findJournalById) | **GET** /journals/{id} | Find Journal by ID
[**findJournals**](JournalApi.md#findJournals) | **GET** /journals | All journal


# **addJournal**
> \Swagger\Client\Model\Journal addJournal($journals)



Creates a new journal in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\JournalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$journals = new \Swagger\Client\Model\JournalInput(); // \Swagger\Client\Model\JournalInput | Journal to add to the system

try {
    $result = $apiInstance->addJournal($journals);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JournalApi->addJournal: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **journals** | [**\Swagger\Client\Model\JournalInput**](../Model/JournalInput.md)| Journal to add to the system |

### Return type

[**\Swagger\Client\Model\Journal**](../Model/Journal.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findJournalById**
> \Swagger\Client\Model\Journal findJournalById($id)

Find Journal by ID

Returns a single journal if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\JournalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of journal to fetch

try {
    $result = $apiInstance->findJournalById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JournalApi->findJournalById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of journal to fetch |

### Return type

[**\Swagger\Client\Model\Journal**](../Model/Journal.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findJournals**
> \Swagger\Client\Model\Journal[] findJournals($tags, $limit)

All journal

Returns all journal from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\JournalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findJournals($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JournalApi->findJournals: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\Journal[]**](../Model/Journal.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

