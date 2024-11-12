# [WOOF! API Reference](overview.md)
## Get a list of all parks
**GET** /park

## (Optional) Query Parameters
| Parameter name   |Type   |Description   |   
|---|---|---|
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| `rating`  |number   | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   

## Sample request

```
{base_url}/park?town=Clinton
```



## Sample response
Status code: `200 OK`

```json
 {
        "park_name": "Bailey's Dog Park",
        "town": "Clinton",
        "coordinates": "41.305547, -72.527168",
        "hours": "5 AM - 5 PM",
        "amenities": "none",
        "comments": "Bring your own everything",
        "rating": "2",
        "id": 5
    }
```
## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
| 201  |Created  | Request successful. The server created a new resource.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
