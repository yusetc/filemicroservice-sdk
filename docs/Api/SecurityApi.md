# Swagger\Client\SecurityApi

All URIs are relative to *https://virtserver.swaggerhub.com/Giffits-Quito/fileservice-sdk/1.1.4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getToken**](SecurityApi.md#getToken) | **POST** /get_token | Authenticate user and obtain token for every operation

# **getToken**
> \Swagger\Client\Model\Token getToken($body)

Authenticate user and obtain token for every operation

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SecurityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\UserData(); // \Swagger\Client\Model\UserData | User data for login

try {
    $result = $apiInstance->getToken($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecurityApi->getToken: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserData**](../Model/UserData.md)| User data for login | [optional]

### Return type

[**\Swagger\Client\Model\Token**](../Model/Token.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

