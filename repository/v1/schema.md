---
description:  
---
# Schema

>  **Package : spaceone.api.repository.v1**

## Schema

{% hint style="info" %}
**Schema Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**create**](schema.md#create)|   [CreateSchemaRequest](schema.md#createschemarequest) |   [SchemaInfo](schema.md#schemainfo) |  |
| 2 | [**update**](schema.md#update)|   [UpdateSchemaRequest](schema.md#updateschemarequest) |   [SchemaInfo](schema.md#schemainfo) |  |
| 3 | [**delete**](schema.md#delete)|   [SchemaRequest](schema.md#schemarequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 4 | [**get**](schema.md#get)|   [GetRepositorySchemaRequest](schema.md#getrepositoryschemarequest) |   [SchemaInfo](schema.md#schemainfo) |  |
| 5 | [**list**](schema.md#list)|   [SchemaQuery](schema.md#schemaquery) |   [SchemasInfo](schema.md#schemasinfo) |  |
| 6 | [**stat**](schema.md#stat)|   [SchemaStatQuery](schema.md#schemastatquery) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  | 
 

 
### create
> **POST** /repository/v1/schemas
>


| Type | Message |
| :--- | :--- |
| Request | [CreateSchemaRequest](schema.md#createschemarequest) |
| Response |  [SchemaInfo](schema.md#schemainfo)  |
 
 

 
### update
> **PUT** /repository/v1/schema/{schema}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdateSchemaRequest](schema.md#updateschemarequest) |
| Response |  [SchemaInfo](schema.md#schemainfo)  |
 
 

 
### delete
> **DELETE** /repository/v1/schema/{schema}
>


| Type | Message |
| :--- | :--- |
| Request | [SchemaRequest](schema.md#schemarequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### get
> **GET** /repository/v1/schemas/{schema}
>


| Type | Message |
| :--- | :--- |
| Request | [GetRepositorySchemaRequest](schema.md#getrepositoryschemarequest) |
| Response |  [SchemaInfo](schema.md#schemainfo)  |
 
 

 
### list
> **GET** /repository/v1/schemas
>
> **POST** /repository/v1/schemas/search



| Type | Message |
| :--- | :--- |
| Request | [SchemaQuery](schema.md#schemaquery) |
| Response |  [SchemasInfo](schema.md#schemasinfo)  |
 
 

 
### stat
> **POST** /repository/v1/schemas/stat
>


| Type | Message |
| :--- | :--- |
| Request | [SchemaStatQuery](schema.md#schemastatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |


## 

## Message

### CreateSchemaRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | service_type |string|✅| |
| 3 | schema |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |
| 4 | labels |[google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview)|❌| |
| 5 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 6 | project_id |string|❌| |
| 7 | domain_id |string|✅| |

### GetRepositorySchemaRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | domain_id |string|✅| |
| 3 | repository_id |string|❌| |
| 4 | only |list of string|❌| |

### SchemaInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | name |string | |
| 2 | service_type |string | |
| 3 | schema |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 4 | labels |[google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview) | |
| 5 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 6 | repository_info |[RepositoryInfo](schema.md#repositoryinfo) | |
| 7 | project_id |string | |
| 8 | domain_id |string | |
| 9 | created_at |string | |
| 10 | updated_at |string | |

### SchemaQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query)|❌| |
| 2 | name |string|❌| |
| 3 | service_type |string|❌| |
| 4 | project_id |string|✅| |
| 5 | repository_id |string|✅| |
| 6 | domain_id |string|✅| |

### SchemaRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | domain_id |string|✅| |

### SchemaStatQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | repository_id |string|✅| |
| 3 | domain_id |string|✅| |

### SchemasInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of SchemaInfo](schema.md#schemainfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### UpdateSchemaRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | schema |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 3 | labels |[google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview)|❌| |
| 4 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 5 | domain_id |string|✅| |
