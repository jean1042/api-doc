---
description:  
---
# Repository

>  **Package : spaceone.api.repository.v1**

## Repository

{% hint style="info" %}
**Repository Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**register**](repository.md#register)|   [CreateRepositoryRequest](repository.md#createrepositoryrequest) |   [RepositoryInfo](repository.md#repositoryinfo) |  |
| 2 | [**update**](repository.md#update)|   [UpdateRepositoryRequest](repository.md#updaterepositoryrequest) |   [RepositoryInfo](repository.md#repositoryinfo) |  |
| 3 | [**deregister**](repository.md#deregister)|   [RepositoryRequest](repository.md#repositoryrequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 4 | [**get**](repository.md#get)|   [GetRepositoryRequest](repository.md#getrepositoryrequest) |   [RepositoryInfo](repository.md#repositoryinfo) |  |
| 5 | [**list**](repository.md#list)|   [RepositoryQuery](repository.md#repositoryquery) |   [RepositoriesInfo](repository.md#repositoriesinfo) |  |
| 6 | [**stat**](repository.md#stat)|   [RepositoryStatQuery](repository.md#repositorystatquery) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  | 
 

 
### register
> **POST** /repository/v1/repositories
>


| Type | Message |
| :--- | :--- |
| Request | [CreateRepositoryRequest](repository.md#createrepositoryrequest) |
| Response |  [RepositoryInfo](repository.md#repositoryinfo)  |
 
 

 
### update
> **PUT** /repository/v1/repository/{repository_id}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdateRepositoryRequest](repository.md#updaterepositoryrequest) |
| Response |  [RepositoryInfo](repository.md#repositoryinfo)  |
 
 

 
### deregister
> **DELETE** /repository/v1/repository/{repository_id}
>


| Type | Message |
| :--- | :--- |
| Request | [RepositoryRequest](repository.md#repositoryrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### get
> **GET** /repository/v1/repositories/{repository_id}
>


| Type | Message |
| :--- | :--- |
| Request | [GetRepositoryRequest](repository.md#getrepositoryrequest) |
| Response |  [RepositoryInfo](repository.md#repositoryinfo)  |
 
 

 
### list
> **GET** /repository/v1/repositories
>
> **POST** /repository/v1/repositories/search



| Type | Message |
| :--- | :--- |
| Request | [RepositoryQuery](repository.md#repositoryquery) |
| Response |  [RepositoriesInfo](repository.md#repositoriesinfo)  |
 
 

 
### stat
> **POST** /repository/v1/repositories/stat
>


| Type | Message |
| :--- | :--- |
| Request | [RepositoryStatQuery](repository.md#repositorystatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |


## 

## Message

### CreateRepositoryRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | repository_type |string|✅| |
| 3 | endpoint |string|❌| |
| 4 | version |string|❌| |
| 5 | secret_id |string|❌| |
| 6 | domain_id |string|✅| |

### GetRepositoryRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository_id |string|✅| |
| 2 | only |list of string|❌| |
| 3 | domain_id |string|✅| |

### RepositoriesInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of RepositoryInfo](repository.md#repositoryinfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### RepositoryInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | repository_id |string | |
| 2 | name |string | |
| 3 | repository_type |string | |
| 4 | endpoint |string | |
| 5 | version |string | |
| 6 | secret_id |string | |
| 7 | created_at |string | |

### RepositoryQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query)|❌| |
| 2 | repository_id |string|❌| |
| 3 | name |string|❌| |
| 4 | repository_type |string|❌| |
| 5 | domain_id |string|✅| |

### RepositoryRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository_id |string|✅| |
| 2 | domain_id |string|✅| |

### RepositoryStatQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | domain_id |string|✅| |

### UpdateRepositoryRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | repository_id |string|✅| |
| 2 | name |string|❌| |
| 3 | domain_id |string|✅| |
