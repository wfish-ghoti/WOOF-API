# [WOOF! API Reference](overview.md)
# `park` resource

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
| `rating`  |number   | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   
| `id`  |number   | The record ID of the pak.  |   

## Endpoints

### Generate a list of all parks

#### Sample request

```
http://localhost:3000/park?town=Clinton
```

#### (Optional) Query Parameters
| Parameter name   |Type   |Description   |   
|---|---|---|
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| `rating`  |number   | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   

#### Sample response
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

### Generate the details of a park by ID

**GET**/park/{id}
#### Sample request

```
http://localhost:3000/park/4
```
#### Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | Park's record ID.   |

#### Sample response
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

### Add a new park record

**POST**/park

#### Sample request
```
http://localhost:3000/park/
```

### Sample body

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

#### Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `park_name`  |string   | The name of the park.  |
| `town`  |string   | Town where the park is located.  |   
| `coordinates`  |number  | Geographic coordinates of the park, as decimal degrees. |   
| hours`  |string   | Opening hours of the park.  |   
| `amenities`  |string  | Brief enumeraton of amenities available to dogs.  |  
| `comments`  |string   | Any additional information about the park.  |   
| `rating`  |number   | Dog owner rating for the pak, on a 1-5 scale, where 1 is poor satisfaction and 5 is very satisfied.  |   

#### Sample response
`201 Created`
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
### Update the details a of dog

**PATCH**/park/{id}

#### Sample request
```
http://localhost:3000/park/6
```

#### Sample body

```json, 
{
   "hours": "9am - 7pm, Veterans Day might affect these hours"
}
```
#### Sample response

Status code: `200 OK`

```json
{
    "park_name": "Indian Ledge Park",
    "town": "Trumbull",
    "coordinates": "41.242874, -73.200669",
    "hours": "9am - 7pm, Veterans Day might affect these hours",
    "amenities": "off-leash area, poo bags, separate areas for small and large dogs",
    "comments": "All dogs must be neutered or spayed to access the park. A Trumbull resident sticker is required for parking.",
    "rating": "4",
    "id": 6
}
```
### Delete the details of a park from WOOF!

**DELETE**/park/{id}

#### Sample request
```
http://localhost:3000/park/6
```

#### Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the park to remove. |  
#### Sample response
Status code: `200 OK`

```json
[]
```

## Related topics
* [dogs](dog-ref.md)
* tutorials
