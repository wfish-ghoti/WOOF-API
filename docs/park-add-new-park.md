# [WOOF! API Reference](overview.md)
## Add a new park 

**POST** /park

## Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `park_name`  |string   | The name of the park.  |
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| `hours`  |string   | Opening hours of the park.  |   
| `amenities`  |string  | Brief enumeraton of amenities available to dogs.  |  
| `comments`  |string   | Any additional information about the park.  |   
| `rating`  |integerr   | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   

## Sample request
```
{base_url}/park
```

## Sample body

```json
{
  "park_name": "Indian Ledge Park",
  "town": "Trumbull",
  "coordinates": "41.242874, -73.200669",
  "hours": "9am - 7pm",
  "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
  "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
  "rating": "4"
}
```

## Sample response
Status code: `201 Created`

```json
{
    "park_name": "Indian Ledge Park",
    "town": "Trumbull",
    "coordinates": "41.242874, -73.200669",
    "hours": "9am - 7pm",
    "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
    "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
    "rating": "4",
    "id": 6
}
```
## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
| 201  |Created  | Request successful. The server created a new resource.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
