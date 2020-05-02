# Create an Event

**URL** : `/api/events/`

**Method** : `POST`

**Auth required** : YES (include token along with request)

**Permissions required** : None

**Request constraints** :

```json
{
    "event_title": "[unicode 64 chars max]",
    "address": "[unicode 500 chars max]",
    "date": "Date",
    "time": "Time",
    "postal_code": "Number",
}
```

## Success Response

**Condition** : If everything is OK and the account is authenticated

**Code** : `201 CREATED`

**Response body example**

```json
{
  "id": "1",
  "author": "John Doe",
  "event_title": "Book fair",
  "date": "05-05-2020",
  "time": "11:00 AM PST",
  "address": "some address",
  "postal_code": "123456"
}
```

## Error Responses

**Condition** : If Account is not authenticated.

**Code** : `401`

**Headers** : `Location: redirect url`

### Or

**Condition** : If fields are missed.

**Code** : `400 BAD REQUEST`

**Response example**

```json
{
    "event_title": [
        "This field is required."
    ]
}
```
