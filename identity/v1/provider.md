---
description:  
---
# Provider

>  **Package : spaceone.api.identity.v1**

## Provider

{% hint style="info" %}
**Provider Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**create**](provider.md#create)|   [CreateProviderRequest](provider.md#createproviderrequest) |   [ProviderInfo](provider.md#providerinfo) |  |
| 2 | [**update**](provider.md#update)|   [UpdateProviderRequest](provider.md#updateproviderrequest) |   [ProviderInfo](provider.md#providerinfo) |  |
| 3 | [**delete**](provider.md#delete)|   [ProviderRequest](provider.md#providerrequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 4 | [**get**](provider.md#get)|   [GetProviderRequest](provider.md#getproviderrequest) |   [ProviderInfo](provider.md#providerinfo) |  |
| 5 | [**list**](provider.md#list)|   [ProviderQuery](provider.md#providerquery) |   [ProvidersInfo](provider.md#providersinfo) |  |
| 6 | [**stat**](provider.md#stat)|   [ProviderStatQuery](provider.md#providerstatquery) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  | 
 

 
### create
> **POST** /identity/v1/providers
>


| Type | Message |
| :--- | :--- |
| Request | [CreateProviderRequest](provider.md#createproviderrequest) |
| Response |  [ProviderInfo](provider.md#providerinfo)  |
 
 

 
### update
> **PUT** /identity/v1/provider/{provider_id}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdateProviderRequest](provider.md#updateproviderrequest) |
| Response |  [ProviderInfo](provider.md#providerinfo)  |
 
 

 
### delete
> **DELETE** /identity/v1/provider/{provider_id}
>


| Type | Message |
| :--- | :--- |
| Request | [ProviderRequest](provider.md#providerrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### get
> **GET** /identity/v1/provider/{provider_id}
>


| Type | Message |
| :--- | :--- |
| Request | [GetProviderRequest](provider.md#getproviderrequest) |
| Response |  [ProviderInfo](provider.md#providerinfo)  |
 
 

 
### list
> **GET** /identity/v1/providers
>
> **POST** /identity/v1/providers/search



| Type | Message |
| :--- | :--- |
| Request | [ProviderQuery](provider.md#providerquery) |
| Response |  [ProvidersInfo](provider.md#providersinfo)  |
 
 

 
### stat
> **POST** /identity/v1/providers/stat
>


| Type | Message |
| :--- | :--- |
| Request | [ProviderStatQuery](provider.md#providerstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |


## 

## Message

### CreateProviderRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider |string|✅| |
| 2 | name |string|✅| |
| 3 | template |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 4 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 5 | capability |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 6 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 7 | domain_id |string|✅| |

### GetProviderRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider |string|✅| |
| 2 | only |list of string|❌| |
| 3 | domain_id |string|✅| |

### ProviderInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | provider |string | |
| 2 | name |string | |
| 3 | template |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 4 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 5 | capability |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 6 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 7 | created_at |string | |

### ProviderQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query)|❌| |
| 2 | provider |string|❌| |
| 3 | name |string|❌| |
| 4 | domain_id |string|✅| |

### ProviderRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider |string|✅| |
| 2 | domain_id |string|✅| |

### ProviderStatQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | domain_id |string|✅| |

### ProvidersInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of ProviderInfo](provider.md#providerinfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### UpdateProviderRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | provider |string|✅| |
| 2 | name |string|❌| |
| 3 | template |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 4 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 5 | capability |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 6 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 7 | domain_id |string|✅| |
