# Swagger\Client\SearchApi

All URIs are relative to *http://api.file.giffits.local*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchMetadataKeyValueGet**](SearchApi.md#searchMetadataKeyValueGet) | **GET** /search/metadata/{key}/{value} | 

# **searchMetadataKeyValueGet**
> \Swagger\Client\Model\FileInfo[] searchMetadataKeyValueGet($key, $value)



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$key = "key_example"; // string | 
$value = "value_example"; // string | 

try {
    $result = $apiInstance->searchMetadataKeyValueGet($key, $value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchMetadataKeyValueGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  |
 **value** | **string**|  |

### Return type

[**\Swagger\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

