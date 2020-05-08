# Swagger\Client\BillOfMaterialsApi

All URIs are relative to *https://bean.ie*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addBillOfMaterial**](BillOfMaterialsApi.md#addBillOfMaterial) | **POST** /bill_of_materials | 
[**findBillOfMaterialById**](BillOfMaterialsApi.md#findBillOfMaterialById) | **GET** /bill_of_materials/{id} | Find Bill of Materials by ID
[**findBillOfMaterials**](BillOfMaterialsApi.md#findBillOfMaterials) | **GET** /bill_of_materials | All bill of materials


# **addBillOfMaterial**
> \Swagger\Client\Model\BillOfMaterial addBillOfMaterial($bill_of_materials)



Creates a new bill of materials in the system

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillOfMaterialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bill_of_materials = new \Swagger\Client\Model\BillOfMaterialInput(); // \Swagger\Client\Model\BillOfMaterialInput | Bill of Materials to add to the system

try {
    $result = $apiInstance->addBillOfMaterial($bill_of_materials);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillOfMaterialsApi->addBillOfMaterial: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bill_of_materials** | [**\Swagger\Client\Model\BillOfMaterialInput**](../Model/BillOfMaterialInput.md)| Bill of Materials to add to the system |

### Return type

[**\Swagger\Client\Model\BillOfMaterial**](../Model/BillOfMaterial.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBillOfMaterialById**
> \Swagger\Client\Model\BillOfMaterial findBillOfMaterialById($id)

Find Bill of Materials by ID

Returns a single bill of materials if the user has access

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillOfMaterialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 789; // int | ID of bill of materials to fetch

try {
    $result = $apiInstance->findBillOfMaterialById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillOfMaterialsApi->findBillOfMaterialById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| ID of bill of materials to fetch |

### Return type

[**\Swagger\Client\Model\BillOfMaterial**](../Model/BillOfMaterial.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findBillOfMaterials**
> \Swagger\Client\Model\BillOfMaterial[] findBillOfMaterials($tags, $limit)

All bill of materials

Returns all bill of materials from the system that the user has access to

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('ApiKey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('ApiKey', 'Bearer');

$apiInstance = new Swagger\Client\Api\BillOfMaterialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tags = array("tags_example"); // string[] | tags to filter by
$limit = 56; // int | Maximum number of results to return

try {
    $result = $apiInstance->findBillOfMaterials($tags, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillOfMaterialsApi->findBillOfMaterials: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tags** | [**string[]**](../Model/string.md)| tags to filter by | [optional]
 **limit** | **int**| Maximum number of results to return | [optional]

### Return type

[**\Swagger\Client\Model\BillOfMaterial[]**](../Model/BillOfMaterial.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

