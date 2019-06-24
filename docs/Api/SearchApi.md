# Swagger\Client\SearchApi

All URIs are relative to *https://virtserver.swaggerhub.com/Giffits-Quito/fileservice-sdk/1.1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchFileByMetadata**](SearchApi.md#searchFileByMetadata) | **GET** /search/metadata/{key}/{value} | Search file by metadata key and value
[**searchFileByMultipleMetadata**](SearchApi.md#searchFileByMultipleMetadata) | **POST** /search/metadata | Search file by multiple metadata passed as json

# **searchFileByMetadata**
> \Swagger\Client\Model\FileInfo[] searchFileByMetadata($key, $value)

Search file by metadata key and value

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = "key_example"; // string | 
$value = "value_example"; // string | 

try {
    $result = $apiInstance->searchFileByMetadata($key, $value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchFileByMetadata: ', $e->getMessage(), PHP_EOL;
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

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **searchFileByMultipleMetadata**
> \Swagger\Client\Model\FileInfo[] searchFileByMultipleMetadata($body)

Search file by multiple metadata passed as json

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Swagger\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\MetadataEntries(); // \Swagger\Client\Model\MetadataEntries | Metadata entries for multi search

try {
    $result = $apiInstance->searchFileByMultipleMetadata($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchFileByMultipleMetadata: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\MetadataEntries**](../Model/MetadataEntries.md)| Metadata entries for multi search | [optional]

### Return type

[**\Swagger\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

