# Entry

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | sgv, mbg, cal, etc | [optional] 
**date_string** | **string** | dateString, prefer ISO &#x60;8601&#x60; | [optional] 
**date** | **float** | Epoch | [optional] 
**sgv** | **float** | The glucose reading. (only available for sgv types) | [optional] 
**direction** | **string** | Direction of glucose trend reported by CGM. (only available for sgv types) | [optional] 
**noise** | **float** | Noise level at time of reading. (only available for sgv types) | [optional] 
**filtered** | **float** | The raw filtered value directly from CGM transmitter. (only available for sgv types) | [optional] 
**unfiltered** | **float** | The raw unfiltered value directly from CGM transmitter. (only available for sgv types) | [optional] 
**rssi** | **float** | The signal strength from CGM transmitter. (only available for sgv types) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


