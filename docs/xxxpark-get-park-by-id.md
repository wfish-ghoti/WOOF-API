# [WOOF! API Reference](overview.md)
## Get the details of a park by ID

**GET** /park/{id}
## Sample request

```
{base_url}/park/4
```
## Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |integer  | Park's record ID.   |

## Sample response
Status code: `200 OK`

```json
{
    "park_name": "Rocky Hill Dog Park",
    "town": "Rocky Hill",
    "coordinates": "41.660178, -72.648414",
    "hours": "6 AM - 6 PM",
    "amenities": "water bowls, poop bags",
    "comments": "Lot of dogs at noon",
    "rating": "4",
    "id": 4
}
```

## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
|200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
