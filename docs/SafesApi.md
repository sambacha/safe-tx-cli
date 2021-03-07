# SafesApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**safesAllTransactionsList**](SafesApi.md#safesAllTransactionsList) | **GET** /safes/{address}/all-transactions/ | 
[**safesBalancesList**](SafesApi.md#safesBalancesList) | **GET** /safes/{address}/balances/ | 
[**safesBalancesUsdList**](SafesApi.md#safesBalancesUsdList) | **GET** /safes/{address}/balances/usd/ | 
[**safesCollectiblesList**](SafesApi.md#safesCollectiblesList) | **GET** /safes/{address}/collectibles/ | 
[**safesCreationList**](SafesApi.md#safesCreationList) | **GET** /safes/{address}/creation/ | 
[**safesDelegatesCreate**](SafesApi.md#safesDelegatesCreate) | **POST** /safes/{address}/delegates/ | 
[**safesDelegatesDelete**](SafesApi.md#safesDelegatesDelete) | **DELETE** /safes/{address}/delegates/{delegate_address}/ | 
[**safesDelegatesList**](SafesApi.md#safesDelegatesList) | **GET** /safes/{address}/delegates/ | 
[**safesIncomingTransactionsList**](SafesApi.md#safesIncomingTransactionsList) | **GET** /safes/{address}/incoming-transactions/ | 
[**safesIncomingTransfersList**](SafesApi.md#safesIncomingTransfersList) | **GET** /safes/{address}/incoming-transfers/ | 
[**safesModuleTransactionsList**](SafesApi.md#safesModuleTransactionsList) | **GET** /safes/{address}/module-transactions/ | 
[**safesMultisigTransactionsCreate**](SafesApi.md#safesMultisigTransactionsCreate) | **POST** /safes/{address}/multisig-transactions/ | 
[**safesMultisigTransactionsList**](SafesApi.md#safesMultisigTransactionsList) | **GET** /safes/{address}/multisig-transactions/ | 
[**safesRead**](SafesApi.md#safesRead) | **GET** /safes/{address}/ | 
[**safesTransactionsCreate**](SafesApi.md#safesTransactionsCreate) | **POST** /safes/{address}/transactions/ | 
[**safesTransactionsList**](SafesApi.md#safesTransactionsList) | **GET** /safes/{address}/transactions/ | 
[**safesTransfersList**](SafesApi.md#safesTransfersList) | **GET** /safes/{address}/transfers/ | 


## **safesAllTransactionsList**



Returns a paginated list of transactions for a Safe. The list has different structures depending on the
transaction type:
- Multisig Transactions for a Safe. 'tx_type=MULTISIG_TRANSACTION'. If the query parameter 'queued=False' is
set only the transactions with 'safe nonce < current Safe nonce' will be displayed. By default, only the
'trusted' transactions will be displayed (transactions indexed, with at least one confirmation or proposed
by a delegate). If you need that behaviour to be disabled set the query parameter 'trusted=False'
- Module Transactions for a Safe. 'tx_type=MODULE_TRANSACTION'
- Incoming Transfers of Ether/ERC20 Tokens/ERC721 Tokens. 'tx_type=ETHEREUM_TRANSACTION'

### Example
```bash
 safesAllTransactionsList address=value  ordering=value  limit=value  offset=value  queued=value  trusted=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **ordering** | **string** | Which field to use when ordering the results. | [optional]
 **limit** | **integer** | Number of results to return per page. | [optional]
 **offset** | **integer** | The initial index from which to return the results. | [optional]
 **queued** | **boolean** | If 'True' transactions with 'nonce >= Safe current nonce' are also returned | [optional] [default to true]
 **trusted** | **boolean** | If 'True' just trusted transactions are shown (indexed, added by a delegate or with at least one confirmation) | [optional] [default to true]

### Return type

[**_AllTransactionsSchema**](_AllTransactionsSchema.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesBalancesList**



Get balance for Ether and ERC20 tokens

### Example
```bash
 safesBalancesList address=value  trusted=value  exclude_spam=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **trusted** | **boolean** | If 'True' just trusted tokens will be returned | [optional] [default to false]
 **excludeSpam** | **boolean** | If 'True' spam tokens will not be returned | [optional] [default to false]

### Return type

[**array[SafeBalanceResponse]**](SafeBalanceResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesBalancesUsdList**



Get balance for Ether and ERC20 tokens with USD fiat conversion

### Example
```bash
 safesBalancesUsdList address=value  trusted=value  exclude_spam=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **trusted** | **boolean** | If 'True' just trusted tokens will be returned | [optional] [default to false]
 **excludeSpam** | **boolean** | If 'True' spam tokens will not be returned | [optional] [default to false]

### Return type

[**array[SafeBalanceUsdResponse]**](SafeBalanceUsdResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesCollectiblesList**



Get collectibles (ERC721 tokens) and information about them

### Example
```bash
 safesCollectiblesList address=value  trusted=value  exclude_spam=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **trusted** | **boolean** | If 'True' just trusted tokens will be returned | [optional] [default to false]
 **excludeSpam** | **boolean** | If 'True' spam tokens will not be returned | [optional] [default to false]

### Return type

[**array[SafeCollectibleResponse]**](SafeCollectibleResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesCreationList**



Get status of the safe

### Example
```bash
 safesCreationList address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |

### Return type

[**SafeCreationInfoResponse**](SafeCreationInfoResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesDelegatesCreate**



Create a delegate for a Safe address with a custom label. Calls with same delegate but different label or
signer will update the label or delegator if different.
For the signature we are using TOTP with 'T0=0' and 'Tx=3600'. TOTP is calculated by taking the
Unix UTC epoch time (no milliseconds) and dividing by 3600 (natural division, no decimals)
For signature this hash need to be signed: keccak(address + str(int(current_epoch // 3600)))
For example:
     - we want to add the owner '0x132512f995866CcE1b0092384A6118EDaF4508Ff' and 'epoch=1586779140'.
     - TOTP = epoch // 3600 = 1586779140 // 3600 = 440771
     - The hash to sign by a Safe owner would be 'keccak(\"0x132512f995866CcE1b0092384A6118EDaF4508Ff440771\")'

### Example
```bash
 safesDelegatesCreate address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **data** | [**SafeDelegate**](SafeDelegate.md) |  |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesDelegatesDelete**



Delete a delegate for a Safe. Signature is built the same way that for adding a delegate.
Check 'POST /delegates/'

### Example
```bash
 safesDelegatesDelete address=value delegate_address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **delegateAddress** | **string** |  |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesDelegatesList**



Get the list of delegates for a Safe address

### Example
```bash
 safesDelegatesList address=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
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

## **safesIncomingTransactionsList**



Returns the history of a multisig tx (safe)

### Example
```bash
 safesIncomingTransactionsList address=value  _from=value  block_number=value  block_number__gt=value  block_number__lt=value  execution_date__gte=value  execution_date__lte=value  execution_date__gt=value  execution_date__lt=value  to=value  token_address=value  transaction_hash=value  value=value  value__gt=value  value__lt=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **from** | **string** |  | [optional]
 **blockNumber** | **integer** |  | [optional]
 **blockNumberGt** | **integer** |  | [optional]
 **blockNumberLt** | **integer** |  | [optional]
 **executionDateGte** | **string** |  | [optional]
 **executionDateLte** | **string** |  | [optional]
 **executionDateGt** | **string** |  | [optional]
 **executionDateLt** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **tokenAddress** | **string** |  | [optional]
 **transactionHash** | **string** |  | [optional]
 **value** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **limit** | **integer** | Number of results to return per page. | [optional]
 **offset** | **integer** | The initial index from which to return the results. | [optional]

### Return type

[**array[TransferResponse]**](TransferResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesIncomingTransfersList**



Returns the history of a multisig tx (safe)

### Example
```bash
 safesIncomingTransfersList address=value  _from=value  block_number=value  block_number__gt=value  block_number__lt=value  execution_date__gte=value  execution_date__lte=value  execution_date__gt=value  execution_date__lt=value  to=value  token_address=value  transaction_hash=value  value=value  value__gt=value  value__lt=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **from** | **string** |  | [optional]
 **blockNumber** | **integer** |  | [optional]
 **blockNumberGt** | **integer** |  | [optional]
 **blockNumberLt** | **integer** |  | [optional]
 **executionDateGte** | **string** |  | [optional]
 **executionDateLte** | **string** |  | [optional]
 **executionDateGt** | **string** |  | [optional]
 **executionDateLt** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **tokenAddress** | **string** |  | [optional]
 **transactionHash** | **string** |  | [optional]
 **value** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **limit** | **integer** | Number of results to return per page. | [optional]
 **offset** | **integer** | The initial index from which to return the results. | [optional]

### Return type

[**array[TransferResponse]**](TransferResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesModuleTransactionsList**



Returns the module transaction of a Safe

### Example
```bash
 safesModuleTransactionsList address=value  safe=value  module=value  to=value  operation=value  failed=value  block_number=value  block_number__gt=value  block_number__lt=value  transaction_hash=value  ordering=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **safe** | **string** |  | [optional]
 **module** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **operation** | **string** |  | [optional]
 **failed** | **string** |  | [optional]
 **blockNumber** | **integer** |  | [optional]
 **blockNumberGt** | **integer** |  | [optional]
 **blockNumberLt** | **integer** |  | [optional]
 **transactionHash** | **string** |  | [optional]
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

## **safesMultisigTransactionsCreate**



Creates a Multisig Transaction with its confirmations and retrieves all the information related.

### Example
```bash
 safesMultisigTransactionsCreate address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **data** | [**SafeMultisigTransaction**](SafeMultisigTransaction.md) |  |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesMultisigTransactionsList**



Returns the history of a multisig tx (safe)

### Example
```bash
 safesMultisigTransactionsList address=value  failed=value  modified__lt=value  modified__gt=value  modified__lte=value  modified__gte=value  nonce__lt=value  nonce__gt=value  nonce__lte=value  nonce__gte=value  nonce=value  safe_tx_hash=value  to=value  value__lt=value  value__gt=value  value=value  executed=value  has_confirmations=value  trusted=value  execution_date__gte=value  execution_date__lte=value  submission_date__gte=value  submission_date__lte=value  transaction_hash=value  ordering=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **failed** | **string** |  | [optional]
 **modifiedLt** | **string** |  | [optional]
 **modifiedGt** | **string** |  | [optional]
 **modifiedLte** | **string** |  | [optional]
 **modifiedGte** | **string** |  | [optional]
 **nonceLt** | **integer** |  | [optional]
 **nonceGt** | **integer** |  | [optional]
 **nonceLte** | **integer** |  | [optional]
 **nonceGte** | **integer** |  | [optional]
 **nonce** | **integer** |  | [optional]
 **safeTxHash** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **value** | **integer** |  | [optional]
 **executed** | **string** |  | [optional]
 **hasConfirmations** | **string** |  | [optional]
 **trusted** | **string** |  | [optional]
 **executionDateGte** | **string** |  | [optional]
 **executionDateLte** | **string** |  | [optional]
 **submissionDateGte** | **string** |  | [optional]
 **submissionDateLte** | **string** |  | [optional]
 **transactionHash** | **string** |  | [optional]
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

## **safesRead**



Get status of the safe

### Example
```bash
 safesRead address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |

### Return type

[**SafeInfoResponse**](SafeInfoResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesTransactionsCreate**



Creates a Multisig Transaction with its confirmations and retrieves all the information related.

### Example
```bash
 safesTransactionsCreate address=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **data** | [**SafeMultisigTransaction**](SafeMultisigTransaction.md) |  |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **safesTransactionsList**



Returns the history of a multisig tx (safe)

### Example
```bash
 safesTransactionsList address=value  failed=value  modified__lt=value  modified__gt=value  modified__lte=value  modified__gte=value  nonce__lt=value  nonce__gt=value  nonce__lte=value  nonce__gte=value  nonce=value  safe_tx_hash=value  to=value  value__lt=value  value__gt=value  value=value  executed=value  has_confirmations=value  trusted=value  execution_date__gte=value  execution_date__lte=value  submission_date__gte=value  submission_date__lte=value  transaction_hash=value  ordering=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **failed** | **string** |  | [optional]
 **modifiedLt** | **string** |  | [optional]
 **modifiedGt** | **string** |  | [optional]
 **modifiedLte** | **string** |  | [optional]
 **modifiedGte** | **string** |  | [optional]
 **nonceLt** | **integer** |  | [optional]
 **nonceGt** | **integer** |  | [optional]
 **nonceLte** | **integer** |  | [optional]
 **nonceGte** | **integer** |  | [optional]
 **nonce** | **integer** |  | [optional]
 **safeTxHash** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **value** | **integer** |  | [optional]
 **executed** | **string** |  | [optional]
 **hasConfirmations** | **string** |  | [optional]
 **trusted** | **string** |  | [optional]
 **executionDateGte** | **string** |  | [optional]
 **executionDateLte** | **string** |  | [optional]
 **submissionDateGte** | **string** |  | [optional]
 **submissionDateLte** | **string** |  | [optional]
 **transactionHash** | **string** |  | [optional]
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

## **safesTransfersList**



Returns the history of a multisig tx (safe)

### Example
```bash
 safesTransfersList address=value  _from=value  block_number=value  block_number__gt=value  block_number__lt=value  execution_date__gte=value  execution_date__lte=value  execution_date__gt=value  execution_date__lt=value  to=value  token_address=value  transaction_hash=value  value=value  value__gt=value  value__lt=value  limit=value  offset=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **from** | **string** |  | [optional]
 **blockNumber** | **integer** |  | [optional]
 **blockNumberGt** | **integer** |  | [optional]
 **blockNumberLt** | **integer** |  | [optional]
 **executionDateGte** | **string** |  | [optional]
 **executionDateLte** | **string** |  | [optional]
 **executionDateGt** | **string** |  | [optional]
 **executionDateLt** | **string** |  | [optional]
 **to** | **string** |  | [optional]
 **tokenAddress** | **string** |  | [optional]
 **transactionHash** | **string** |  | [optional]
 **value** | **integer** |  | [optional]
 **valueGt** | **integer** |  | [optional]
 **valueLt** | **integer** |  | [optional]
 **limit** | **integer** | Number of results to return per page. | [optional]
 **offset** | **integer** | The initial index from which to return the results. | [optional]

### Return type

[**array[TransferResponse]**](TransferResponse.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

