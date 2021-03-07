# MultisigTransactionsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**multisigTransactionsConfirmationsCreate**](MultisigTransactionsApi.md#multisigTransactionsConfirmationsCreate) | **POST** /multisig-transactions/{safe_tx_hash}/confirmations/ | 
[**multisigTransactionsConfirmationsList**](MultisigTransactionsApi.md#multisigTransactionsConfirmationsList) | **GET** /multisig-transactions/{safe_tx_hash}/confirmations/ | 
[**multisigTransactionsRead**](MultisigTransactionsApi.md#multisigTransactionsRead) | **GET** /multisig-transactions/{safe_tx_hash}/ | 


## **multisigTransactionsConfirmationsCreate**



Add a confirmation for a transaction. More than one signature can be used. This endpoint does not support
the use of delegates to make a transaction trusted.

### Example
```bash
 multisigTransactionsConfirmationsCreate safe_tx_hash=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **safeTxHash** | **string** |  |
 **data** | [**SafeMultisigConfirmation**](SafeMultisigConfirmation.md) |  |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **multisigTransactionsConfirmationsList**



Get the list of confirmations for a multisig transaction

### Example
```bash
 multisigTransactionsConfirmationsList safe_tx_hash=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **safeTxHash** | **string** |  |
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

## **multisigTransactionsRead**





### Example
```bash
 multisigTransactionsRead safe_tx_hash=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **safeTxHash** | **string** |  |

### Return type

[**SafeMultisigTransactionResponse**](SafeMultisigTransactionResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

