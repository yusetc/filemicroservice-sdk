# Swagger\Client\FileApi

All URIs are relative to *http://api.file.giffits.local*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addFile**](FileApi.md#addFile) | **POST** /media | Add a new file to the filesystem
[**deleteFile**](FileApi.md#deleteFile) | **DELETE** /media/{id} | Deletes a file
[**downloadFile**](FileApi.md#downloadFile) | **GET** /media/download/{id} | Download a file with a specific id
[**findAllFiles**](FileApi.md#findAllFiles) | **GET** /media | Get all files
[**findFileById**](FileApi.md#findFileById) | **GET** /media/{id} | Get file by ID
[**patchFile**](FileApi.md#patchFile) | **PATCH** /media | Patch a specific file from the filesystem
[**updateFile**](FileApi.md#updateFile) | **PUT** /media | Update a specific file from the filesystem

# **addFile**
> \Swagger\Client\Model\FileInfo addFile($body)

Add a new file to the filesystem

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\FileDataPost(); // \Swagger\Client\Model\FileDataPost | File data to add

try {
    $result = $apiInstance->addFile($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->addFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\FileDataPost**](../Model/FileDataPost.md)| File data to add | [optional]

### Return type

[**\Swagger\Client\Model\FileInfo**](../Model/FileInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteFile**
> deleteFile($id)

Deletes a file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | 

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

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **downloadFile**
> string downloadFile($id)

Download a file with a specific id

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | 

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

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-streamapplication/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findAllFiles**
> \Swagger\Client\Model\FileInfo[] findAllFiles($limit, $offset)

Get all files

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
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

[**\Swagger\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **findFileById**
> \Swagger\Client\Model\FileInfo findFileById($id)

Get file by ID

Returns a single file

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | File identifier

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

[**\Swagger\Client\Model\FileInfo**](../Model/FileInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchFile**
> \Swagger\Client\Model\FileInfo[] patchFile($body)

Patch a specific file from the filesystem

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\FileObject(); // \Swagger\Client\Model\FileObject | File data to update

try {
    $result = $apiInstance->patchFile($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->patchFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\FileObject**](../Model/FileObject.md)| File data to update | [optional]

### Return type

[**\Swagger\Client\Model\FileInfo[]**](../Model/FileInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateFile**
> \Swagger\Client\Model\FileObject[] updateFile($body)

Update a specific file from the filesystem

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\FileObject(); // \Swagger\Client\Model\FileObject | File data to update

try {
    $result = $apiInstance->updateFile($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->updateFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\FileObject**](../Model/FileObject.md)| File data to update | [optional]

### Return type

[**\Swagger\Client\Model\FileObject[]**](../Model/FileObject.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

