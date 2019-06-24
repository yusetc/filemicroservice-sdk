# OpenAPI\Client\FileApi

All URIs are relative to *https://virtserver.swaggerhub.com/Giffits-Quito/fileservice-sdk/1.1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addFile**](FileApi.md#addFile) | **POST** /media | Add a new file to the filesystem
[**deleteFile**](FileApi.md#deleteFile) | **DELETE** /media/{id} | Deletes a file
[**downloadFile**](FileApi.md#downloadFile) | **GET** /media/download/{id} | Download a file with a specific id
[**findAllFiles**](FileApi.md#findAllFiles) | **GET** /media | Get all files
[**findFileById**](FileApi.md#findFileById) | **GET** /media/{id} | Get file by ID
[**patchFile**](FileApi.md#patchFile) | **PATCH** /media | Patch a specific file from the filesystem
[**updateFile**](FileApi.md#updateFile) | **PUT** /media | Update a specific file from the filesystem



## addFile

> \OpenAPI\Client\Model\FileInfo addFile($fileDataPost)

Add a new file to the filesystem

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fileDataPost = new \OpenAPI\Client\Model\FileDataPost(); // \OpenAPI\Client\Model\FileDataPost | File data to add

try {
    $result = $apiInstance->addFile($fileDataPost);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->addFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileDataPost** | [**\OpenAPI\Client\Model\FileDataPost**](../Model/FileDataPost.md)| File data to add | [optional]

### Return type

[**\OpenAPI\Client\Model\FileInfo**](../Model/FileInfo.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## deleteFile

> deleteFile($id)

Deletes a file

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 

try {
    $apiInstance->deleteFile($id);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->deleteFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)|  |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## downloadFile

> \SplFileObject downloadFile($id)

Download a file with a specific id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->downloadFile($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->downloadFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)|  |

### Return type

[**\SplFileObject**](../Model/\SplFileObject.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## findAllFiles

> \OpenAPI\Client\Model\FileInfo[] findAllFiles($limit, $offset)

Get all files

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 56; // int | Amount of elements per page
$offset = 56; // int | Page offset

try {
    $result = $apiInstance->findAllFiles($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->findAllFiles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Amount of elements per page | [optional]
 **offset** | **int**| Page offset | [optional]

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


## findFileById

> \OpenAPI\Client\Model\FileInfo findFileById($id)

Get file by ID

Returns a single file

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | File identifier

try {
    $result = $apiInstance->findFileById($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->findFileById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| File identifier |

### Return type

[**\OpenAPI\Client\Model\FileInfo**](../Model/FileInfo.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## patchFile

> \OpenAPI\Client\Model\FileObject patchFile($fileObject)

Patch a specific file from the filesystem

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fileObject = new \OpenAPI\Client\Model\FileObject(); // \OpenAPI\Client\Model\FileObject | File data to update

try {
    $result = $apiInstance->patchFile($fileObject);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->patchFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileObject** | [**\OpenAPI\Client\Model\FileObject**](../Model/FileObject.md)| File data to update | [optional]

### Return type

[**\OpenAPI\Client\Model\FileObject**](../Model/FileObject.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## updateFile

> \OpenAPI\Client\Model\FileObject updateFile($fileObject)

Update a specific file from the filesystem

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$fileObject = new \OpenAPI\Client\Model\FileObject(); // \OpenAPI\Client\Model\FileObject | File data to update

try {
    $result = $apiInstance->updateFile($fileObject);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->updateFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileObject** | [**\OpenAPI\Client\Model\FileObject**](../Model/FileObject.md)| File data to update | [optional]

### Return type

[**\OpenAPI\Client\Model\FileObject**](../Model/FileObject.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

