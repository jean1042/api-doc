---
description:  
---
# Data source

>  **Package : spaceone.api.billing.v1**

## DataSource

{% hint style="info" %}
**DataSource Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**register**](data-source.md#register)|   [RegisterDataSourceRequest](data-source.md#registerdatasourcerequest) |   [DataSourceInfo](data-source.md#datasourceinfo) |  |
| 2 | [**update**](data-source.md#update)|   [UpdateDataSourceRequest](data-source.md#updatedatasourcerequest) |   [DataSourceInfo](data-source.md#datasourceinfo) |  |
| 3 | [**enable**](data-source.md#enable)|   [DataSourceRequest](data-source.md#datasourcerequest) |   [DataSourceInfo](data-source.md#datasourceinfo) |  |
| 4 | [**disable**](data-source.md#disable)|   [DataSourceRequest](data-source.md#datasourcerequest) |   [DataSourceInfo](data-source.md#datasourceinfo) |  |
| 5 | [**deregister**](data-source.md#deregister)|   [DataSourceRequest](data-source.md#datasourcerequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 6 | [**verify_plugin**](data-source.md#verify_plugin)|   [DataSourceRequest](data-source.md#datasourcerequest) |   [VerifyInfo](data-source.md#verifyinfo) |  |
| 7 | [**get**](data-source.md#get)|   [GetDataSourceRequest](data-source.md#getdatasourcerequest) |   [DataSourceInfo](data-source.md#datasourceinfo) |  |
| 8 | [**list**](data-source.md#list)|   [DataSourceQuery](data-source.md#datasourcequery) |   [DataSourcesInfo](data-source.md#datasourcesinfo) |  |
| 9 | [**stat**](data-source.md#stat)|   [DataSourceStatQuery](data-source.md#datasourcestatquery) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  | 
 

 
### register
> **POST** /billing/v1/data-sources
>


| Type | Message |
| :--- | :--- |
| Request | [RegisterDataSourceRequest](data-source.md#registerdatasourcerequest) |
| Response |  [DataSourceInfo](data-source.md#datasourceinfo)  |
 
 

 
### update
> **PUT** /billing/v1/data-source/{data_source_id}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdateDataSourceRequest](data-source.md#updatedatasourcerequest) |
| Response |  [DataSourceInfo](data-source.md#datasourceinfo)  |
 
 

 
### enable
> **PUT** /billing/v1/data-source/{data_source_id}/enable
>


| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](data-source.md#datasourcerequest) |
| Response |  [DataSourceInfo](data-source.md#datasourceinfo)  |
 
 

 
### disable
> **PUT** /billing/v1/data-source/{data_source_id}/disable
>


| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](data-source.md#datasourcerequest) |
| Response |  [DataSourceInfo](data-source.md#datasourceinfo)  |
 
 

 
### deregister
> **DELETE** /billing/v1/data-source/{data_source_id}
>


| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](data-source.md#datasourcerequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### verify_plugin
> **PUT** /billing/v1/data-source/{data_source_id}/plugin/verify
>


| Type | Message |
| :--- | :--- |
| Request | [DataSourceRequest](data-source.md#datasourcerequest) |
| Response |  [VerifyInfo](data-source.md#verifyinfo)  |
 
 

 
### get
> **GET** /billing/v1/data-source/{data_source_id}
>


| Type | Message |
| :--- | :--- |
| Request | [GetDataSourceRequest](data-source.md#getdatasourcerequest) |
| Response |  [DataSourceInfo](data-source.md#datasourceinfo)  |
 
 

 
### list
> **GET** /billing/v1/data-sources
>
> **POST** /billing/v1/data-sources/search



| Type | Message |
| :--- | :--- |
| Request | [DataSourceQuery](data-source.md#datasourcequery) |
| Response |  [DataSourcesInfo](data-source.md#datasourcesinfo)  |
 
 

 
### stat
> **POST** /billing/v1/data-sources/stat
>


| Type | Message |
| :--- | :--- |
| Request | [DataSourceStatQuery](data-source.md#datasourcestatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |


## 

## Message

### DataSourceInfo
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">data_source_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left"><ul>
          	<li>NONE</li>
          	<li>ENABLED</li>
          	<li>DISABLED</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">capability</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">plugin_info</td>
      <td style="text-align:left"><a href="data-source.md#plugininfo">PluginInfo</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### DataSourceQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query)|❌| |
| 2 | data_source_id |string|❌| |
| 3 | name |string|❌| |
| 4 | state |string|❌| |
| 5 | provider |string|❌| |
| 6 | domain_id |string|✅| |

### DataSourceRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data_source_id |string|✅| |
| 2 | domain_id |string|✅| |

### DataSourceStatQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | domain_id |string|✅| |

### DataSourcesInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of DataSourceInfo](data-source.md#datasourceinfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### GetDataSourceRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data_source_id |string|✅| |
| 2 | domain_id |string|✅| |
| 3 | only |list of string|❌| |

### PluginInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | plugin_id |string | |
| 2 | version |string | |
| 3 | options |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |
| 4 | secret_id |string | |
| 5 | provider |string | |
| 6 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |

### RegisterDataSourceRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | plugin_info |[PluginInfo](data-source.md#plugininfo)|✅| |
| 3 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 4 | domain_id |string|✅| |

### UpdateDataSourceRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | data_source_id |string|✅| |
| 2 | name |string|❌| |
| 3 | plugin_info |[PluginInfo](data-source.md#plugininfo)|❌| |
| 4 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 5 | domain_id |string|✅| |

### VerifyInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | status |bool | |
