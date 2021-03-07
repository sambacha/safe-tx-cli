# ContractsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contractsList**](ContractsApi.md#contractsList) | **GET** /contracts/ | 
[**contractsRead**](ContractsApi.md#contractsRead) | **GET** /contracts/{address}/ | 


## **contractsList**





### Example
```bash
 contractsList  ordering=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ordering** | **string** | Which field to use when ordering the results. | [optional]
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

## **contractsRead**





### Example
```bash
 contractsRead address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** | A unique value identifying this contract. |

### Return type

[**Contract**](Contract.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

