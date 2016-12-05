# Swagger\Client\StatusApi

All URIs are relative to the host set in property $host in Swagger\Client\Configuration

Method | HTTP request | Description
------------- | ------------- | -------------
[**statusGet**](StatusApi.md#statusGet) | **GET** /status | Status


# **statusGet**
> \Swagger\Client\Model\Status statusGet()

Status

Server side status, default settings and capabilities.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_secret
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api_secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api_secret', 'Bearer');
Swagger\Client\Configuration::getDefaultConfiguration()setHost('https://{YOUR_NS_SITE}/api/v1');

$api_instance = new Swagger\Client\Api\StatusApi();

try {
    $result = $api_instance->statusGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusApi->statusGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Status**](../Model/Status.md)

### Authorization

[api_secret](../../README.md#api_secret)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

