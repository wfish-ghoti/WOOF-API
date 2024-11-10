# [WOOF! API Reference](overview.md)
# `dog` resource

Base endpoint:

```
{server_url}/dog
```

**Dog** contains details about the dog(s) registered in the WOOF! API. 

## Resource properties
Sampe `dog` resource

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

|Property name   |Type   |Description   |   
|---|---|---|
| `name`  |string   | The name of the dog.  |
| `photo`  |string   | File path to the dog's photo.  |   
| `breed`  |string   | The record ID of the user.  |   
| `size`  |string   | The size category of the dog: small, medium, lerge.  |   
| `human`  |string  | The name of the owner or person in charge. Multiple values allowed if comma separated. Can be full name or first name only.  |   
| `something_about_yourself`  |string   | A short description of the dog's character personality.  |   
| `at_the_park_?`  |boolean   | Whether the dog is at the park right now: True/False. Default value is False. |   
| `park_idd`  |number   | The record ID of the park.  |   
| `id`  |number   | The record ID of the dog.  |   

## Endpoints

### Generate a list of all ldogs

**GET**/dog

#### Sample request

#### Parameters

#### Sample response

### Generate the details of a dog by ID

**GET**/dog/{id}
#### Sample request

#### Parameters

|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the dog.   |   

#### Sample response

#### Sample request

#### Parameters

#### Sample response


### Add a new dog record

**POST**/dog

#### Sample request

#### Parameters

#### Sample response


### Update the details a of dog

**PUT**/dog/{id}

#### Sample request

#### Parameters

#### Sample response


### Delete the details of a dog from WOOF!

**DELETE**/dog/{id}

#### Sample request
```
DELETE/dog/3
```
#### Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `id`  |number   | The record ID of the dog to remove. |  
#### Sample response
XXXXXXXXXX


