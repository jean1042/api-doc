---
description:  
---
# Spot group

>  **Package : spaceone.api.spot_automation.v1**

## SpotGroup

{% hint style="info" %}
**SpotGroup Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**create**](spot-group.md#create)|   [CreateSpotGroupRequest](spot-group.md#createspotgrouprequest) |   [SpotGroupInfo](spot-group.md#spotgroupinfo) |  |
| 2 | [**update**](spot-group.md#update)|   [UpdateSpotGroupRequest](spot-group.md#updatespotgrouprequest) |   [SpotGroupInfo](spot-group.md#spotgroupinfo) |  |
| 3 | [**delete**](spot-group.md#delete)|   [SpotGroupRequest](spot-group.md#spotgrouprequest) |  [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|  |
| 4 | [**get**](spot-group.md#get)|   [GetSpotGroupRequest](spot-group.md#getspotgrouprequest) |   [SpotGroupInfo](spot-group.md#spotgroupinfo) |  |
| 5 | [**list**](spot-group.md#list)|   [QuerySpotGroupRequest](spot-group.md#queryspotgrouprequest) |   [SpotGroupsInfo](spot-group.md#spotgroupsinfo) |  |
| 6 | [**stat**](spot-group.md#stat)|   [SpotGroupStatRequest](spot-group.md#spotgroupstatrequest) |  [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|  |
| 7 | [**get_candidates**](spot-group.md#get_candidates)|   [GetCandidatesRequest](spot-group.md#getcandidatesrequest) |   [CandidatesInfo](spot-group.md#candidatesinfo) |  | 
 

 
### create
> **POST** /spot-automation/v1/spot-groups
>


| Type | Message |
| :--- | :--- |
| Request | [CreateSpotGroupRequest](spot-group.md#createspotgrouprequest) |
| Response |  [SpotGroupInfo](spot-group.md#spotgroupinfo)  |
 
 

 
### update
> **PUT** /spot-automation/v1/spot-group/{spot_group_id}
>


| Type | Message |
| :--- | :--- |
| Request | [UpdateSpotGroupRequest](spot-group.md#updatespotgrouprequest) |
| Response |  [SpotGroupInfo](spot-group.md#spotgroupinfo)  |
 
 

 
### delete
> **DELETE** /spot-automation/v1/spot-group/{spot_group_id}
>


| Type | Message |
| :--- | :--- |
| Request | [SpotGroupRequest](spot-group.md#spotgrouprequest) |
| Response | [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto) |
 
 

 
### get
> **GET** /spot-automation/v1/spot-group/{spot_group_id}
>


| Type | Message |
| :--- | :--- |
| Request | [GetSpotGroupRequest](spot-group.md#getspotgrouprequest) |
| Response |  [SpotGroupInfo](spot-group.md#spotgroupinfo)  |
 
 

 
### list
> **GET** /spot-automation/v1/spot-groups
>
> **POST** /spot-automation/v1/spot-groups/search



| Type | Message |
| :--- | :--- |
| Request | [QuerySpotGroupRequest](spot-group.md#queryspotgrouprequest) |
| Response |  [SpotGroupsInfo](spot-group.md#spotgroupsinfo)  |
 
 

 
### stat
> **POST** /spot-automation/v1/spot-groups/stat
>


| Type | Message |
| :--- | :--- |
| Request | [SpotGroupStatRequest](spot-group.md#spotgroupstatrequest) |
| Response | [google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) |
 
 

 
### get_candidates
> **GET** /spot-automation/v1/spot-group/candidates
>


| Type | Message |
| :--- | :--- |
| Request | [GetCandidatesRequest](spot-group.md#getcandidatesrequest) |
| Response |  [CandidatesInfo](spot-group.md#candidatesinfo)  |


## 

## Message

### CandidateInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | type |string | |
| 2 | priority |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### CandidatesInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of CandidateInfo](spot-group.md#candidateinfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### CreateSpotGroupRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | name |string|✅| |
| 2 | resource_id |string|✅| |
| 3 | resource_type |string|✅| |
| 4 | options |[SpotGroupOptions](spot-group.md#spotgroupoptions)|❌| |
| 5 | tags |list of spaceone.api.core.v1.Tag|❌| |
| 6 | user_id |string|✅| |
| 7 | domain_id |string|✅| |

### GetCandidatesRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | resource_id |string|✅| |
| 2 | resource_type |string|✅| |
| 3 | domain_id |string|✅| |

### GetSpotGroupRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | spot_group_id |string|✅| |
| 2 | domain_id |string|✅| |
| 3 | only |list of string|❌| |

### QuerySpotGroupRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.Query](https://spaceone-dev.gitbook.io/api-reference/common-v1/search-query)|❌| |
| 2 | spot_group_id |string|❌| |
| 3 | name |string|❌| |
| 4 | resource_id |string|❌| |
| 5 | resource_type |string|❌| |
| 6 | provider |string|❌| |
| 7 | project_id |string|❌| |
| 8 | region_code |string|❌| |
| 9 | domain_id |string|✅| |

### SpotGroupInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | spot_group_id |string | |
| 2 | name |string | |
| 3 | resource_id |string | |
| 4 | resource_type |string | |
| 5 | region_code |string | |
| 6 | provider |string | |
| 7 | cloud_service_group |string | |
| 8 | cloud_service_type |string | |
| 9 | reference |[SpotGroupResourceReference](spot-group.md#spotgroupresourcereference) | |
| 10 | options |[SpotGroupOptions](spot-group.md#spotgroupoptions) | |
| 11 | project_id |string | |
| 12 | tags |list of spaceone.api.core.v1.Tag | |
| 13 | domain_id |string | |
| 14 | created_by |string | |
| 15 | created_at |[google.protobuf.Timestamp](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/timestamp.proto) | |

### SpotGroupOptions
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
      <td style="text-align:left">min_ondemand_size</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">min_ondemand_ratio</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto">int32</a></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">recommend_types</td>
      <td style="text-align:left">list of string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">replace_strategy</td>
      <td style="text-align:left"><ul>
          	<li>CHEAPEST</li>
          	<li>OPTIMAL</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### SpotGroupRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | spot_group_id |string|✅| |
| 2 | domain_id |string|✅| |

### SpotGroupResourceReference
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | resource_id |string | |
| 2 | external_link |string | |

### SpotGroupStatRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | query |[spaceone.api.core.v1.StatisticsQuery](https://spaceone-dev.gitbook.io/api-reference/common-v1/statistics-query)|✅| |
| 2 | domain_id |string|✅| |

### SpotGroupsInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | results |[list of SpotGroupInfo](spot-group.md#spotgroupinfo) | |
| 2 | total_count |[int32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### UpdateSpotGroupRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | spot_group_id |string|✅| |
| 2 | name |string|❌| |
| 3 | options |[SpotGroupOptions](spot-group.md#spotgroupoptions)|❌| |
| 4 | tags |list of spaceone.api.core.v1.Tag|❌| |
| 5 | domain_id |string|✅| |