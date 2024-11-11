# [WOOF! API Reference](overview.md)
# `dog` resource

Base endpoint:

```
{server_url}/dog
```

**Dog** contains details about the dog(s) registered in the WOOF! API. 

## Resource properties
Sample `dog` resource

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

**Note:** All properties are required.

|Parameter name   |Type   |Description   |   
|---|---|---|
| `name`  |string   | The name of the dog.  |
| `photo`  |string   | File path to the dog's photo.  |   
| `breed`  |string   | The record ID of the user.  |   
| `size`  |string   | The size category of the dog: Small, Medium, Large.  |   
| `human`  |string  | The name of the owner or person in charge. Multiple values allowed if comma separated. Can be full name or first name only.  | 
| `zip_code`  |string   | Zip Code where dog and humans reside.  |   
| `something_about_yourself`  |string   | A short description of the dog's character personality.  |   
| `at_the_park_?`  |string   | Whether the dog is at the park right now: True/False. Default value is False. |   
| `park_idd`  |number   | The record ID of the park.  |   
| `id`  |number   | The record ID of the dog.  |   

## Endpoints

### Generate a list of all ldogs

**GET**/dog

#### Sample request

```
http://localhost:3000/dog?size=Medium
```

#### (Optional) Query Parameters
| Parameter name   |Type   |Description   |   
|---|---|---|
| `size`  |string   | Dog size category.  |  
| `zip_code`  |string   | Zip code where dog and humans reside.  |   
| `at_the_park_?`  |boolean   | Is the dog currently present at the park? |   

#### Sample response
Status code: `200 OK`

```json
 {
        "name": "Oona",
        "photo": "../Photos/Oona.jpeg",
        "breed": "Anatolian/Heeler mix",
        "size": "Medium",
        "human": "Diane & Matthias",
        "zip_code": "06443",
        "something_about_yourself": "I never met a dog I didn't like!",
        "at_the_park_?": "Y",
        "park_id": 4,
        "id": 5
    }
```

### Generate the details of a dog by ID

**GET**/dog/{id}
#### Sample request
```
http://localhost:3000/dog/4
```
#### Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | Filter by the dog's record ID.   |   

#### Sample response
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


### Add a new dog record

**POST**/dog

#### Sample request
```
http://localhost:3000/dog/
```

### Sample body

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

#### Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `name`  |string   | The name of the dog.  |
| `photo`  |string   | File path to the dog's photo.  |   
| `breed`  |string   | The record ID of the user.  |   
| `size`  |string   | The size category of the dog: Small, Medium, Large.  |   
| `human`  |string  | The name of the owner or person in charge. Multiple values allowed if comma separated. Can be full name or first name only.  | 
| `zip_code`  |string   | Zip Code where dog and humans reside.  |   
| `something_about_yourself`  |string   | A short description of the dog's character personality.  |   
| `at_the_park_?`  |string   | Whether the dog is at the park right now: True/False. Default value is False. |   
| `park_idd`  |number   | The record ID of the park.  |    

#### Sample response
`201 Created`
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
    "id": 9
}
```
### Update the details a of dog

**PATCH**/dog/{id}

#### Sample request
```
http://localhost:3000/dog/9
```

#### Sample body
Status code: `200 OK`

```json
{
  "name": "Beckett Jr"
}
```
#### Parameters

#### Sample response
```json
{
    "name": "Beckett Jr.",
    "photo": "../Photos/Beckett.jpeg",
    "breed": "Irish Wolfhound",
    "size": "Large",
    "human": "Samuel and Suzanne",
    "zip_code": "06040",
    "something_about_yourself": "Plays tough with big guys and gentle with little ones.",
    "at_the_park_?": "N",
    "park_id": 4,
    "id": 9
}
```
### Delete the details of a dog from WOOF!

**DELETE**/dog/{id}
#### Sample request
```
http://localhost:3000/dog/8
```
#### Sample request
```
DELETE/dog/3
```
#### Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the dog to remove. |  
#### Sample response
Status code: `200 OK`

```json
[]
```

## Related topics
* parks
* tutorials

