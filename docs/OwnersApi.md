# OwnersApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ownersRead**](OwnersApi.md#ownersRead) | **GET** /owners/{address}/ | 


## **ownersRead**



Return Safes where the address provided is an owner

### Example
```bash
 ownersRead address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |

### Return type

[**OwnerResponse**](OwnerResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

