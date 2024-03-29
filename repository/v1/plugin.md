---
description:  
---
# Plugin

>  **Package : spaceone.api.repository.v1**

## Plugin

{% hint style="info" %}
**Plugin Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**register**](plugin.md#register)|   [CreatePluginRequest](plugin.md#createpluginrequest) |   [PluginInfo](plugin.md#plugininfo) |  |
| 2 | [**update**](plugin.md#update)|   [UpdatePluginRequest](plugin.md#updatepluginrequest) |   [PluginInfo](plugin.md#plugininfo) |  |
| 3 | [**deregister**](plugin.md#deregister)|   [PluginRequest](plugin.md#pluginrequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 4 | [**enable**](plugin.md#enable)|   [PluginRequest](plugin.md#pluginrequest) |   [PluginInfo](plugin.md#plugininfo) |  |
| 5 | [**disable**](plugin.md#disable)|   [PluginRequest](plugin.md#pluginrequest) |   [PluginInfo](plugin.md#plugininfo) |  |
| 6 | [**get_versions**](plugin.md#get_versions)|   [RepositoryPluginRequest](plugin.md#repositorypluginrequest) |   [VersionsInfo](plugin.md#versionsinfo) |  |
| 7 | [**get**](plugin.md#get)|   [GetRepositoryPluginRequest](plugin.md#getrepositorypluginrequest) |   [PluginInfo](plugin.md#plugininfo) |  |
| 8 | [**list**](plugin.md#list)|   [PluginQuery](plugin.md#pluginquery) |   [PluginsInfo](plugin.md#pluginsinfo) |  |
| 9 | [**stat**](plugin.md#stat)|   [PluginStatQuery](plugin.md#pluginstatquery) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  | 
 

 
### register
> **POST** /repository/v1/plugins
>


| Type | Message |
| :--- | :--- |
| Request | [CreatePluginRequest](plugin.md#createpluginrequest) |
| Response |  [PluginInfo](plugin.md#plugininfo)  |
 
 

 
### update
> **PUT** /repository/v1/plugin/{plugin_id}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdatePluginRequest](plugin.md#updatepluginrequest) |
| Response |  [PluginInfo](plugin.md#plugininfo)  |
 
 

 
### deregister
> **DELETE** /repository/v1/plugin/{plugin_id}
>


| Type | Message |
| :--- | :--- |
| Request | [PluginRequest](plugin.md#pluginrequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### enable
> **PUT** /repository/v1/plugin/{plugin_id}/enable
>


| Type | Message |
| :--- | :--- |
| Request | [PluginRequest](plugin.md#pluginrequest) |
| Response |  [PluginInfo](plugin.md#plugininfo)  |
 
 

 
### disable
> **PUT** /repository/v1/plugin/{plugin_id}/disable
>


| Type | Message |
| :--- | :--- |
| Request | [PluginRequest](plugin.md#pluginrequest) |
| Response |  [PluginInfo](plugin.md#plugininfo)  |
 
 

 
### get_versions
> **GET** /repository/v1/plugins/{plugin_id}/versions
>


| Type | Message |
| :--- | :--- |
| Request | [RepositoryPluginRequest](plugin.md#repositorypluginrequest) |
| Response |  [VersionsInfo](plugin.md#versionsinfo)  |
 
 

 
### get
> **GET** /repository/v1/plugins/{plugin_id}
>


| Type | Message |
| :--- | :--- |
| Request | [GetRepositoryPluginRequest](plugin.md#getrepositorypluginrequest) |
| Response |  [PluginInfo](plugin.md#plugininfo)  |
 
 

 
### list
> **GET** /repository/v1/plugins
>
> **POST** /repository/v1/plugins/search



| Type | Message |
| :--- | :--- |
| Request | [PluginQuery](plugin.md#pluginquery) |
| Response |  [PluginsInfo](plugin.md#pluginsinfo)  |
 
 

 
### stat
> **POST** /repository/v1/plugins/stat
>


| Type | Message |
| :--- | :--- |
| Request | [PluginStatQuery](plugin.md#pluginstatquery) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |


## 

## Message

### CreatePluginRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | service_type |string|✅| |
| 3 | image |string|✅| |
| 4 | provider |string|❌| |
| 5 | capability |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 6 | template |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 7 | labels |[google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview)|❌| |
| 8 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 9 | project_id |string|❌| |
| 10 | domain_id |string|✅| |

### GetRepositoryPluginRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin_id |string|✅| |
| 2 | domain_id |string|✅| |
| 3 | repository_id |string|❌| |
| 4 | only |list of string|❌| |

### PluginInfo
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
      <td style="text-align:left">plugin_id</td>
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
      <td style="text-align:left">image</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">registry_url</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left"><ul>
          	<li>NONE</li>
          	<li>ENABLED</li>
          	<li>DISABLED</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">service_type</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">capability</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">template</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">labels</td>
      <td style="text-align:left"><a href="https://developers.google.com/protocol-buffers/docs/reference/overview">google.protobuf.ListValue</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">tags</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">repository_info</td>
      <td style="text-align:left"><a href="plugin.md#repositoryinfo">RepositoryInfo</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">project_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">15</td>
      <td style="text-align:left">created_at</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">16</td>
      <td style="text-align:left">updated_at</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### PluginQuery
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Required</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">query</td>
      <td style="text-align:left"><a href="https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query">spaceone.api.core.v1.Query</a></td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">plugin_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left"><ul>
          	<li>NONE</li>
          	<li>ENABLED</li>
          	<li>DISABLED</li>
        </ul></td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">service_type</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">provider</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">❌</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">repository_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">✅</td>
<td style="text-align:left"></td>
   </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">domain_id</td>
      <td style="text-align:left">string</td>
<td style="text-align:left">✅</td>
<td style="text-align:left"></td>
   </tr>
  </tbody>
</table>



### PluginRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin_id |string|✅| |
| 2 | domain_id |string|✅| |

### PluginStatQuery
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | repository_id |string|✅| |
| 3 | domain_id |string|✅| |

### PluginsInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of PluginInfo](plugin.md#plugininfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### RepositoryPluginRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin_id |string|✅| |
| 2 | domain_id |string|✅| |
| 3 | repository_id |string|❌| |

### UpdatePluginRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | plugin_id |string|✅| |
| 2 | name |string|❌| |
| 3 | capability |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 4 | template |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 5 | labels |[google.protobuf.ListValue](https://developers.google.com/protocol-buffers/docs/reference/overview)|❌| |
| 6 | tags |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|❌| |
| 7 | domain_id |string|✅| |

### VersionsInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | version |list of string | deprecated field|
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |
| 3 | results |list of string | |
