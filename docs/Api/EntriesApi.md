# Swagger\Client\EntriesApi

All URIs are relative to the host set in property $host in Swagger\Client\Configuration

Method | HTTP request | Description
------------- | ------------- | -------------
[**addEntries**](EntriesApi.md#addEntries) | **POST** /entries | Add new entries.
[**echoStorageSpecGet**](EntriesApi.md#echoStorageSpecGet) | **GET** /echo/{storage}/{spec} | View generated Mongo Query object
[**entriesGet**](EntriesApi.md#entriesGet) | **GET** /entries | All Entries matching query
[**entriesSpecGet**](EntriesApi.md#entriesSpecGet) | **GET** /entries/{spec} | All Entries matching query
[**remove**](EntriesApi.md#remove) | **DELETE** /entries | Delete entries matching query.
[**sliceStorageFieldTypePrefixRegexGet**](EntriesApi.md#sliceStorageFieldTypePrefixRegexGet) | **GET** /slice/{storage}/{field}/{type}/{prefix}/{regex} | All Entries matching query
[**timesEchoPrefixRegexGet**](EntriesApi.md#timesEchoPrefixRegexGet) | **GET** /times/echo/{prefix}/{regex} | Echo the query object to be used.
[**timesPrefixRegexGet**](EntriesApi.md#timesPrefixRegexGet) | **GET** /times/{prefix}/{regex} | All Entries matching query


# **addEntries**
> addEntries($body)

Add new entries.



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');


$api_instance = new Swagger\Client\Api\EntriesApi();
$body = new \Swagger\Client\Model\Entries(); // \Swagger\Client\Model\Entries | Entries to be uploaded.

try {
    $api_instance->addEntries($body);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->addEntries: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Entries**](../Model/\Swagger\Client\Model\Entries.md)| Entries to be uploaded. |

### Return type

void (empty response body)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: application/json, text/plain
 - **Accept**: application/json, text/plain

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

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
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');


$api_instance = new Swagger\Client\Api\EntriesApi();
$storage = "storage_example"; // string | `entries`, or `treatments` to select the storage layer.
$spec = "spec_example"; // string | entry id, such as `55cf81bc436037528ec75fa5` or a type filter such as `sgv`, `mbg`, etc. This parameter is optional.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->echoStorageSpecGet($storage, $spec, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->echoStorageSpecGet: ', $e->getMessage(), PHP_EOL;
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

# **entriesGet**
> \Swagger\Client\Model\Entries entriesGet($find, $count)

All Entries matching query

The Entries endpoint returns information about the Nightscout entries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->entriesGet($find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->entriesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\Entries**](../Model/Entries.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **entriesSpecGet**
> \Swagger\Client\Model\Entries entriesSpecGet($spec, $find, $count)

All Entries matching query

The Entries endpoint returns information about the Nightscout entries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$spec = "spec_example"; // string | entry id, such as `55cf81bc436037528ec75fa5` or a type filter such as `sgv`, `mbg`, etc.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->entriesSpecGet($spec, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->entriesSpecGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **spec** | **string**| entry id, such as &#x60;55cf81bc436037528ec75fa5&#x60; or a type filter such as &#x60;sgv&#x60;, &#x60;mbg&#x60;, etc. |
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\Entries**](../Model/Entries.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **remove**
> remove($find, $count)

Delete entries matching query.

Remove entries, same search syntax as GET.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $api_instance->remove($find, $count);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->remove: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

void (empty response body)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sliceStorageFieldTypePrefixRegexGet**
> \Swagger\Client\Model\Entries sliceStorageFieldTypePrefixRegexGet($storage, $field, $type, $prefix, $regex, $find, $count)

All Entries matching query

The Entries endpoint returns information about the Nightscout entries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$storage = "storage_example"; // string | Prefix to use in constructing a prefix-based regex, default is `entries`.
$field = "field_example"; // string | Name of the field to use Regex against in query object, default is `dateString`.
$type = "type_example"; // string | The type field to search against, default is sgv.
$prefix = "prefix_example"; // string | Prefix to use in constructing a prefix-based regex.
$regex = "regex_example"; // string | Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: `T{15..17}:.*`, this would search for all records from 3pm to 5pm.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->sliceStorageFieldTypePrefixRegexGet($storage, $field, $type, $prefix, $regex, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->sliceStorageFieldTypePrefixRegexGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **storage** | **string**| Prefix to use in constructing a prefix-based regex, default is &#x60;entries&#x60;. |
 **field** | **string**| Name of the field to use Regex against in query object, default is &#x60;dateString&#x60;. |
 **type** | **string**| The type field to search against, default is sgv. |
 **prefix** | **string**| Prefix to use in constructing a prefix-based regex. |
 **regex** | **string**| Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: &#x60;T{15..17}:.*&#x60;, this would search for all records from 3pm to 5pm. |
 **find** | **string**| The query used to find entries, support nested query syntax, for example &#x60;find[dateString][$gte]&#x3D;2015-08-27&#x60;.  All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\Entries**](../Model/Entries.md)

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
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$prefix = "prefix_example"; // string | Prefix to use in constructing a prefix-based regex.
$regex = "regex_example"; // string | Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: `T{15..17}:.*`, this would search for all records from 3pm to 5pm.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->timesEchoPrefixRegexGet($prefix, $regex, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->timesEchoPrefixRegexGet: ', $e->getMessage(), PHP_EOL;
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

# **timesPrefixRegexGet**
> \Swagger\Client\Model\Entries timesPrefixRegexGet($prefix, $regex, $find, $count)

All Entries matching query

The Entries endpoint returns information about the Nightscout entries.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\EntriesApi();
$prefix = "prefix_example"; // string | Prefix to use in constructing a prefix-based regex.
$regex = "regex_example"; // string | Tail part of regexp to use in expanding/construccting a query object. Regexp also has bash-style brace and glob expansion applied to it, creating ways to search for modal times of day, perhaps using something like this syntax: `T{15..17}:.*`, this would search for all records from 3pm to 5pm.
$find = "find_example"; // string | The query used to find entries, support nested query syntax, for example `find[dateString][$gte]=2015-08-27`.  All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->timesPrefixRegexGet($prefix, $regex, $find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntriesApi->timesPrefixRegexGet: ', $e->getMessage(), PHP_EOL;
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

[**\Swagger\Client\Model\Entries**](../Model/Entries.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

