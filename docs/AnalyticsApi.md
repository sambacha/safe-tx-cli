# AnalyticsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyticsMultisigTransactionsByOriginList**](AnalyticsApi.md#analyticsMultisigTransactionsByOriginList) | **GET** /analytics/multisig-transactions/by-origin/ | 
[**analyticsMultisigTransactionsBySafeList**](AnalyticsApi.md#analyticsMultisigTransactionsBySafeList) | **GET** /analytics/multisig-transactions/by-safe/ | 


## **analyticsMultisigTransactionsByOriginList**





### Example
```bash
 analyticsMultisigTransactionsByOriginList  safe=value  to=value  value__lt=value  value__gt=value  value__lte=value  value__gte=value  value=value  operation=value  failed=value  safe_tx_gas__lt=value  safe_tx_gas__gt=value  safe_tx_gas__lte=value  safe_tx_gas__gte=value  safe_tx_gas=value  base_gas__lt=value  base_gas__gt=value  base_gas__lte=value  base_gas__gte=value  base_gas=value  gas_price__lt=value  gas_price__gt=value  gas_price__lte=value  gas_price__gte=value  gas_price=value  gas_token=value  refund_receiver=value  trusted=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **safe** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **valueLte** | **integer** |  | [optional]
 **valueGte** | **integer** |  | [optional]
 **value** | **integer** |  | [optional]
 **operation** | **string** |  | [optional]
 **failed** | **string** |  | [optional]
 **safeTxGasLt** | **integer** |  | [optional]
 **safeTxGasGt** | **integer** |  | [optional]
 **safeTxGasLte** | **integer** |  | [optional]
 **safeTxGasGte** | **integer** |  | [optional]
 **safeTxGas** | **integer** |  | [optional]
 **baseGasLt** | **integer** |  | [optional]
 **baseGasGt** | **integer** |  | [optional]
 **baseGasLte** | **integer** |  | [optional]
 **baseGasGte** | **integer** |  | [optional]
 **baseGas** | **integer** |  | [optional]
 **gasPriceLt** | **integer** |  | [optional]
 **gasPriceGt** | **integer** |  | [optional]
 **gasPriceLte** | **integer** |  | [optional]
 **gasPriceGte** | **integer** |  | [optional]
 **gasPrice** | **integer** |  | [optional]
 **gasToken** | **string** |  | [optional]
 **refundReceiver** | **string** |  | [optional]
 **trusted** | **string** |  | [optional]

### Return type

[**array[AnalyticsMultisigTxsByOriginResponse]**](AnalyticsMultisigTxsByOriginResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **analyticsMultisigTransactionsBySafeList**





### Example
```bash
 analyticsMultisigTransactionsBySafeList  master_copy=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **masterCopy** | **string** |  | [optional]
 **limit** | **integer** | Number of results to return per page. | [optional]
 **offset** | **integer** | The initial index from which to return the results. | [optional]

### Return type

**map**

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

