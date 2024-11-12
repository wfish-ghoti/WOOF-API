# [WOOF! API Reference](overview.md)
## Update the details a of dog

**PUT** /park/{id}

## Sample request
```
{base_url}/park/6
```

## Sample body

```json, 
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

## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
|200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
