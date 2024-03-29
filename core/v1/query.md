---
description:  
---
# Query

>  **Package : spaceone.api.core.v1**

## 

## Message

### AggregateCount
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | name |string | |

### AggregateGroup
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | keys |[list of AggregateGroupKey](query.md#aggregategroupkey) | |
| 2 | fields |[list of AggregateGroupField](query.md#aggregategroupfield) | |

### AggregateGroupField
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | key |string | |
| 2 | k |string | |
| 3 | name |string | |
| 4 | n |string | |
| 5 | operator |string | |
| 6 | o |string | |
| 7 | value |string | |
| 8 | v |string | |
| 9 | date_format |string | |

### AggregateGroupKey
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | key |string | |
| 2 | k |string | |
| 3 | name |string | |
| 4 | n |string | |
| 5 | date_format |string | |

### AggregateSort
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | key |string | |
| 2 | desc |bool | |

### AggregateUnwind
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | path |string | |

### Filter
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | key |string | |
| 2 | k |string | |
| 3 | value |[google.protobuf.Value](https://developers.google.com/protocol-buffers/docs/reference/overview) | |
| 4 | v |[google.protobuf.Value](https://developers.google.com/protocol-buffers/docs/reference/overview) | |
| 5 | operator |string | |
| 6 | o |string | |

### Page
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | start |[uint32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |
| 2 | limit |[uint32](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/type.proto) | |

### Query
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | filter |[list of Filter](query.md#filter) | |
| 2 | filter_or |[list of Filter](query.md#filter) | |
| 3 | sort |[Sort](query.md#sort) | |
| 4 | page |[Page](query.md#page) | |
| 5 | minimal |bool | |
| 6 | count_only |bool | |
| 7 | only |list of string | |
| 8 | keyword |string | |

### Sort
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | key |string | |
| 2 | desc |bool | |

### StatisticsAggregate
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | unwind |[AggregateUnwind](query.md#aggregateunwind) | |
| 2 | group |[AggregateGroup](query.md#aggregategroup) | |
| 3 | count |[AggregateCount](query.md#aggregatecount) | |
| 4 | sort |[AggregateSort](query.md#aggregatesort) | |

### StatisticsQuery
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | filter |[list of Filter](query.md#filter) | |
| 2 | filter_or |[list of Filter](query.md#filter) | |
| 3 | aggregate |[list of StatisticsAggregate](query.md#statisticsaggregate) | |
| 4 | page |[Page](query.md#page) | |
| 5 | distinct |string | |
| 6 | keyword |string | |
