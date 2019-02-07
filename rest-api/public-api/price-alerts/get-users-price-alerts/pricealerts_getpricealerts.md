# Syntax

## Get price alerts

```text
GET /v{version}/users/{userId}/pricealerts
```

### Description

Provides price alerts collection related to specified user

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | Bearer type token string | string |  |
| **Header** | **Et-App-Key**   _required_ | Application key | string |  |
| **Path** | **userId**   _required_ | User identifier | integer \(int32\) |  |
| **Path** | **version**   _required_ | The requested API version | string | `"1"` |
| **Query** | **isDesc**   _required_ | Sorting direction. Desc if true, otherwise is asc | boolean |  |
| **Query** | **pageNumber**   _required_ | Page number | integer \(int32\) |  |
| **Query** | **pageSize**   _required_ | Page size | integer \(int32\) |  |
| **Query** | **sortBy**   _required_ | Sorting field | string |  |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | Price alerts collection | [PagingResult\[PriceAlertInfoModel\]](pricealerts_getpricealerts.md#pagingresult-pricealertinfomodel) |
| **401** | Authorization has been denied for this request. | No Content |
| **403** | Application key is not defined or does not exist | No Content |
| **422** | Validation error occurred while processing entity | No Content |
| **500** | Internal server error | No Content |

### Produces

* `application/json`
* `text/json`
