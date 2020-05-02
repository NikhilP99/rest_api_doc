# Show Nearby Events

Get the details of the currently Authenticated User along with basic
subscription information.

**URL** : `/api/events/`

**Method** : `GET`

**Auth required** : NO

**Query parameters (if any)** :
* near (Optional): postal code of a location
* date (Optional): date in DD-MM-YYYY format

**Sample request** : `/api/events/?near=123456&date:05-05-2020`

## Success Response

**Code** : `200 OK`

**Response examples**

An array of objects satisfying the constraints provided in the query

```json
[
  {
    "id": "1",
    "author": "John Doe",
    "event_title": "Book fair",
    "date": "05-05-2020",
    "time": "11:00 AM PST",
    "address": "some address",
    "postal_code": "123456"
  },
  {
    "id": "2",
    "author": "John Doe",
    "event_title": "Book fair 1",
    "date": "05-05-2020",
    "time": "2:00 PM PST",
    "address": "some address",
    "postal_code": "123876"
  },
  ...
]
```

## Notes

* If no query param is provided, it will return all events scheduled for next 3 days.
