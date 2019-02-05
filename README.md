# File-Microservice SDK
SDK to consume API files Microservice

- API version: 1.0.0-oas3
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\FileDataForSend(); // \Swagger\Client\Model\FileDataForSend | File data to add

try {
    $result = $apiInstance->addFile($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->addFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *http://api.file.giffits.local/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FileApi* | [**addFile**](docs/Api/FileApi.md#addfile) | **POST** /media | Add a new file to the filesystem
*FileApi* | [**deleteFile**](docs/Api/FileApi.md#deletefile) | **DELETE** /media/{id} | Deletes a file
*FileApi* | [**downloadFile**](docs/Api/FileApi.md#downloadfile) | **GET** /media/download/{id} | Download a file from specific id
*FileApi* | [**findAllFiles**](docs/Api/FileApi.md#findallfiles) | **GET** /media | Find all files
*FileApi* | [**findFileById**](docs/Api/FileApi.md#findfilebyid) | **GET** /media/{id} | Find file by ID
*FileApi* | [**patchFile**](docs/Api/FileApi.md#patchfile) | **PATCH** /media | Patch a specific file from the filesystem
*FileApi* | [**updateFile**](docs/Api/FileApi.md#updatefile) | **PUT** /media | Update a specific file from the filesystem
*SearchApi* | [**searchMetadataKeyValueGet**](docs/Api/SearchApi.md#searchmetadatakeyvalueget) | **GET** /search/metadata/{key}/{value} | 

## Documentation For Models

 - [FileDataForSend](docs/Model/FileDataForSend.md)
 - [FileInfo](docs/Model/FileInfo.md)
 - [FileObject](docs/Model/FileObject.md)
 - [GeneralError](docs/Model/GeneralError.md)
 - [MetadataEntry](docs/Model/MetadataEntry.md)
 - [MetadataInfo](docs/Model/MetadataInfo.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author


