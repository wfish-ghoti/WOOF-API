# [WOOF! API Reference](overview.md)
## Remove a park

**DELETE** /park/{id}

## Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the park to remove. |  

## Sample request
```
{base_url}/park/6
```


## Sample response

Status code: `200 OK`

Returns an empty `park` object.

```json
{}
```

## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
