# Swagger\Client\ProfileApi

All URIs are relative to the host set in property $host in Swagger\Client\Configuration

Method | HTTP request | Description
------------- | ------------- | -------------
[**profileGet**](ProfileApi.md#profileGet) | **GET** /profile | Profile


# **profileGet**
> \Swagger\Client\Model\Profile profileGet()

Profile

The Profile endpoint returns information about the Nightscout Treatment Profiles.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');

$api_instance = new Swagger\Client\Api\ProfileApi();

try {
    $result = $api_instance->profileGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProfileApi->profileGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Profile**](../Model/Profile.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

