# Swagger\Client\DebugApi

All URIs are relative to *https://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**echoStorageSpecGet**](DebugApi.md#echoStorageSpecGet) | **GET** /echo/{storage}/{spec} | View generated Mongo Query object
[**timesEchoPrefixRegexGet**](DebugApi.md#timesEchoPrefixRegexGet) | **GET** /times/echo/{prefix}/{regex} | Echo the query object to be used.


# **echoStorageSpecGet**
> \Swagger\Client\Model\MongoQuery echoStorageSpecGet($storage, $spec, $find, $count)

View generated Mongo Query object

Information about the mongo query object created by the query.

### Example
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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage** | **string**| &#x60;entries&#x60;, or &#x60;treatments&#x60; to select the storage layer. |
 **spec** | **string**| entry id, such as &#x60;55cf81bc436037528ec75fa5&#x60; or a type filter such as &#x60;sgv&#x60;, &#x60;mbg&#x60;, etc. This parameter is optional. |
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\MongoQuery**](../Model/MongoQuery.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **timesEchoPrefixRegexGet**
> \Swagger\Client\Model\MongoQuery timesEchoPrefixRegexGet($prefix, $regex, $find, $count)

Echo the query object to be used.

Echo debug information about the query object constructed.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$api_instance = new Swagger\Client\Api\DebugApi();
$prefix = "prefix_example"; // string | Prefix to use in constructing a prefix-based regex.
$regex = "regex_example"; // string | Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: `T{15..17}:.*`, this would search for all records from 3pm to 5pm.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->timesEchoPrefixRegexGet($prefix, $regex, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DebugApi->timesEchoPrefixRegexGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **prefix** | **string**| Prefix to use in constructing a prefix-based regex. |
 **regex** | **string**| Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: &#x60;T{15..17}:.*&#x60;, this would search for all records from 3pm to 5pm. |
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\MongoQuery**](../Model/MongoQuery.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

