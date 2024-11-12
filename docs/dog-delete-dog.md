# [WOOF! API Reference](overview.md)
## Remove a dog 
Delete the details of a `dog` from the WOOF! API.

**DELETE** /dog/{id}

## Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the dog to remove. |  

## Sample request
```
{base_url}/dog/3
```

## Sample response
Returns an empty array.

Status code: `200 OK`

```json
[]
```
## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
