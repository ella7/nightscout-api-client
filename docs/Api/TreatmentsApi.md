# Swagger\Client\TreatmentsApi

All URIs are relative to the host set in property $host in Swagger\Client\Configuration

Method | HTTP request | Description
------------- | ------------- | -------------
[**addTreatments**](TreatmentsApi.md#addTreatments) | **POST** /treatments | Add new treatments.
[**treatmentsGet**](TreatmentsApi.md#treatmentsGet) | **GET** /treatments | Treatments


# **addTreatments**
> addTreatments($body)

Add new treatments.



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$api_instance = new Swagger\Client\Api\TreatmentsApi();
$body = new \Swagger\Client\Model\Treatments(); // \Swagger\Client\Model\Treatments | Treatments to be uploaded.

try {
    $api_instance->addTreatments($body);
} catch (Exception $e) {
    echo 'Exception when calling TreatmentsApi->addTreatments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Treatments**](../Model/\Swagger\Client\Model\Treatments.md)| Treatments to be uploaded. |

### Return type

void (empty response body)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **treatmentsGet**
> \Swagger\Client\Model\Treatments treatmentsGet($find, $count)

Treatments

The Treatments endpoint returns information about the Nightscout treatments.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$api_instance = new Swagger\Client\Api\TreatmentsApi();
$find = "find_example"; // string | The query used to find entries, supports nested query syntax.  Examples `find[insulin][$gte]=3` `find[carb][$gte]=100` `find[eventType]=Correction+Bolus` All find parameters are interpreted as strings.
$count = 3.4; // float | Number of entries to return.

try {
    $result = $api_instance->treatmentsGet($find, $count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TreatmentsApi->treatmentsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **find** | **string**| The query used to find entries, supports nested query syntax.  Examples &#x60;find[insulin][$gte]&#x3D;3&#x60; &#x60;find[carb][$gte]&#x3D;100&#x60; &#x60;find[eventType]&#x3D;Correction+Bolus&#x60; All find parameters are interpreted as strings. | [optional]
 **count** | **float**| Number of entries to return. | [optional]

### Return type

[**\Swagger\Client\Model\Treatments**](../Model/Treatments.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

