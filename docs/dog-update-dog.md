# [WOOF! API Reference](overview.md)
## Update the details a of dog
Change any of the proprties for a `dog`.

**PUT** /dog/{id}

## Sample request
```
{base_url}/dog/8
```

## Sample body

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
    "park_id": 3
}
```

## Sample response
Returns the update `dog` record.
Status code: `200 OK`

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
    "id": 8
}
```
