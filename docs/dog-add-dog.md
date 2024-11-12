# [WOOF! API Reference](overview.md)
## Add a new dog
Create a new catalogue entry for a dog.

**POST** /dog

## Sample request
```
{base_url}/dog/
```

## Sample body

```json
{
    "name": "Beckett",
    "photo": "../Photos/Beckett.jpeg",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 3
}
```
## Sample response
Status code: `201 Created`
```json
{
    "name": "Beckett",
    "photo": "../Photos/Beckett.jpeg",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 3,
    "id": 8
}
```
  ## Response status
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
| 201 |Created  | Request successful. The server has created a new resource.  | 
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|
