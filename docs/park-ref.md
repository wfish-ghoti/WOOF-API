# [WOOF! API Reference](overview.md)
## `park` resource

Base endpoint:

```
{server_url}/park
```

**Park** contains details about the (dog) parks registered in the WOOF! API. 

```json
{
  "park_name": "Paw Dog Park",
  "town": "Essex",
  "coordinates": "41.335345, -72.398537",
  "hours": "temporarily closed",
  "amenities": "small dog area, poop bags",
  "comments": "must park in upper lot between December and April",
  "rating": "2",
  "id": 2
}
```

|Property name   |Type   |Description   |   
|---|---|---|
| `park_name`  |string   | The name of the park.  |
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| hours`  |string   | Opening hours of the park.  |   
| `amenities`  |string  | Brief enumeraton of amenities available to dogs.  |  
| `comments`  |string   | Any additional information about the park.  |   
| `rating`  |integer  | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   
| `id`  |integer  | The record ID of the pak.  |   


## Endpoints
* [Get all parks](park-get-all-parks.md)
* [Get park by ID](park-get-park-by-id.md)
* [Add park](park-add-new-park.md)
* [Update park](park-update-park.md)
* [Remove park](park-delete-park.md)

## Related topics
* [dogs](dog-ref.md)
* tutorials
