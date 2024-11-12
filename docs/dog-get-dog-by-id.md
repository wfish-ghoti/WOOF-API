# [WOOF! API Reference](overview.md)
## Get the details of a dog by ID

Get the catalogue details of a single dog identified by its unique ID.

**GET** /dog/{id}

## Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The ID of the dog record to be updated.   |  

## Sample request
```
{base_url}/dog/4
``` 

## Sample response
Returns the details of the dog identified by its unique ID.

Status code: `200 OK`

```json
{
    "name": "Loki",
    "photo": "../Photos/Loki.jpeg",
    "breed": "Siberian Husky",
    "size": "Large",
    "human": "Sylvana",
    "zip_code": "06040",
    "something_about_yourself": "As long as no balls are involved, I'm very mellow!",
    "at_the_park_?": "N",
    "park_id": 1,
    "id": 4
}
```


## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
