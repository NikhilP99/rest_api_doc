# Show Current User

Get the details of the currently Authenticated User along with basic
subscription information.

**URL** : `/api/user/`

**Method** : `GET`

**Auth required** : YES (Authentication token to be included with request)

**Query parameters (if any)** : `NONE`

## Success Response

**Code** : `200 OK`

**Response examples**

For a User with ID 1234 on the local database where that User has saved an
email address and name information.

```json
{
    "id": 1234,
    "first_name": "Joe",
    "last_name": "Bloggs",
    "email": "joe25@example.com"
}
```

## Notes

* Special note of any.
