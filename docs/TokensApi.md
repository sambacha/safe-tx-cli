# TokensApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tokensList**](TokensApi.md#tokensList) | **GET** /tokens/ | 
[**tokensRead**](TokensApi.md#tokensRead) | **GET** /tokens/{address}/ | 


## **tokensList**





### Example
```bash
 tokensList  name=value  address=value  symbol=value  decimals__lt=value  decimals__gt=value  decimals=value  search=value  ordering=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string** |  | [optional]
 **address** | **string** |  | [optional]
 **symbol** | **string** |  | [optional]
 **decimalsLt** | **integer** |  | [optional]
 **decimalsGt** | **integer** |  | [optional]
 **decimals** | **integer** |  | [optional]
 **search** | **string** | A search term. | [optional]
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

## **tokensRead**





### Example
```bash
 tokensRead address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** | A unique value identifying this token. |

### Return type

[**TokenInfoResponse**](TokenInfoResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

