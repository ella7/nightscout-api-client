# SwaggerClient-php
Own your DData with the Nightscout API

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.8.0
- Build package: class io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.4.0 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com//.git"
    }
  ],
  "require": {
    "/": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/autoload.php');
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

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$api_instance = new Swagger\Client\Api\DebugApi();
$storage = "storage_example"; // string | `entries`, or `treatments` to select the storage layer.
$spec = "spec_example"; // string | entry id, such as `55cf81bc436037528ec75fa5` or a type filter such as `sgv`, `mbg`, etc. This parameter is optional.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->echoStorageSpecGet($storage, $spec, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DebugApi->echoStorageSpecGet: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://localhost/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DebugApi* | [**echoStorageSpecGet**](docs/Api/DebugApi.md#echostoragespecget) | **GET** /echo/{storage}/{spec} | View generated Mongo Query object
*DebugApi* | [**timesEchoPrefixRegexGet**](docs/Api/DebugApi.md#timesechoprefixregexget) | **GET** /times/echo/{prefix}/{regex} | Echo the query object to be used.
*EntriesApi* | [**addEntries**](docs/Api/EntriesApi.md#addentries) | **POST** /entries | Add new entries.
*EntriesApi* | [**echoStorageSpecGet**](docs/Api/EntriesApi.md#echostoragespecget) | **GET** /echo/{storage}/{spec} | View generated Mongo Query object
*EntriesApi* | [**entriesGet**](docs/Api/EntriesApi.md#entriesget) | **GET** /entries | All Entries matching query
*EntriesApi* | [**entriesSpecGet**](docs/Api/EntriesApi.md#entriesspecget) | **GET** /entries/{spec} | All Entries matching query
*EntriesApi* | [**remove**](docs/Api/EntriesApi.md#remove) | **DELETE** /entries | Delete entries matching query.
*EntriesApi* | [**sliceStorageFieldTypePrefixRegexGet**](docs/Api/EntriesApi.md#slicestoragefieldtypeprefixregexget) | **GET** /slice/{storage}/{field}/{type}/{prefix}/{regex} | All Entries matching query
*EntriesApi* | [**timesEchoPrefixRegexGet**](docs/Api/EntriesApi.md#timesechoprefixregexget) | **GET** /times/echo/{prefix}/{regex} | Echo the query object to be used.
*EntriesApi* | [**timesPrefixRegexGet**](docs/Api/EntriesApi.md#timesprefixregexget) | **GET** /times/{prefix}/{regex} | All Entries matching query
*ProfileApi* | [**profileGet**](docs/Api/ProfileApi.md#profileget) | **GET** /profile | Profile
*StatusApi* | [**statusGet**](docs/Api/StatusApi.md#statusget) | **GET** /status | Status
*TreatmentsApi* | [**addTreatments**](docs/Api/TreatmentsApi.md#addtreatments) | **POST** /treatments | Add new treatments.
*TreatmentsApi* | [**treatmentsGet**](docs/Api/TreatmentsApi.md#treatmentsget) | **GET** /treatments | Treatments


## Documentation For Models

 - [Entries](docs/Model/Entries.md)
 - [Entry](docs/Model/Entry.md)
 - [Error](docs/Model/Error.md)
 - [ExtendedSettings](docs/Model/ExtendedSettings.md)
 - [MongoQuery](docs/Model/MongoQuery.md)
 - [Profile](docs/Model/Profile.md)
 - [Settings](docs/Model/Settings.md)
 - [Status](docs/Model/Status.md)
 - [Threshold](docs/Model/Threshold.md)
 - [Treatment](docs/Model/Treatment.md)
 - [Treatments](docs/Model/Treatments.md)


## Documentation For Authorization


## api_secret

- **Type**: API key
- **API key parameter name**: api_secret
- **Location**: HTTP header


## Author




