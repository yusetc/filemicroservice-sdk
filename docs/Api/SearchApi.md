# OpenAPI\Client\SearchApi

All URIs are relative to *https://virtserver.swaggerhub.com/Giffits-Quito/fileservice-sdk/1.1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**searchByKeyMetadata**](SearchApi.md#searchByKeyMetadata) | **GET** /search/all/{key} | Search file by metadata key
[**searchFileByMetadata**](SearchApi.md#searchFileByMetadata) | **GET** /search/metadata/{key}/{value} | Search file by metadata key and value
[**searchFileByMultipleMetadata**](SearchApi.md#searchFileByMultipleMetadata) | **POST** /search/metadata | Search file by multiple metadata passed as json



## searchByKeyMetadata

> \OpenAPI\Client\Model\KeyData[] searchByKeyMetadata($key)

Search file by metadata key

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string | 

try {
    $result = $apiInstance->searchByKeyMetadata($key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchByKeyMetadata: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  |

### Return type

[**\OpenAPI\Client\Model\KeyData[]**](../Model/KeyData.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## searchFileByMetadata

> \OpenAPI\Client\Model\FileInfo[] searchFileByMetadata($key, $value)

Search file by metadata key and value

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = 'key_example'; // string | 
$value = 'value_example'; // string | 

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

[**\OpenAPI\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## searchFileByMultipleMetadata

> \OpenAPI\Client\Model\FileInfo[] searchFileByMultipleMetadata($metadataEntries)

Search file by multiple metadata passed as json

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$metadataEntries = new \OpenAPI\Client\Model\MetadataEntries(); // \OpenAPI\Client\Model\MetadataEntries | Metadata entries for multi search

try {
    $result = $apiInstance->searchFileByMultipleMetadata($metadataEntries);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->searchFileByMultipleMetadata: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metadataEntries** | [**\OpenAPI\Client\Model\MetadataEntries**](../Model/MetadataEntries.md)| Metadata entries for multi search | [optional]

### Return type

[**\OpenAPI\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

