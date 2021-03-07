# NotificationsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**notificationsDevicesCreate**](NotificationsApi.md#notificationsDevicesCreate) | **POST** /notifications/devices/ | 
[**notificationsDevicesDelete**](NotificationsApi.md#notificationsDevicesDelete) | **DELETE** /notifications/devices/{uuid}/ | 
[**notificationsDevicesSafesDelete**](NotificationsApi.md#notificationsDevicesSafesDelete) | **DELETE** /notifications/devices/{uuid}/safes/{address}/ | 


## **notificationsDevicesCreate**



Creates a new FirebaseDevice. If uuid is not provided a new device will be created.
If a uuid for an existing Safe is provided the FirebaseDevice will be updated with all the new data provided.
Safes provided on the request are always added and never removed/replaced

### Example
```bash
 notificationsDevicesCreate
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**FirebaseDevice**](FirebaseDevice.md) |  |

### Return type

[**FirebaseDevice**](FirebaseDevice.md)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **notificationsDevicesDelete**



Remove a FirebaseDevice

### Example
```bash
 notificationsDevicesDelete uuid=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**string**](.md) | A UUID string identifying this Firebase Device. |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **notificationsDevicesSafesDelete**



Remove a Safe for a FirebaseDevice

### Example
```bash
 notificationsDevicesSafesDelete address=value uuid=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **address** | **string** |  |
 **uuid** | [**string**](.md) | A UUID string identifying this Firebase Device. |

### Return type

(empty response body)

### Authorization

[Basic](../README.md#Basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

