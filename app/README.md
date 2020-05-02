# REST API Doc

## Endpoints

### Auth
* [Login](auth/login.md) : `POST /api/login/`

### User related
Each endpoint manipulates or displays information related to the User whose id is provided with the request:

* [Show info](user/get.md) : `GET /api/user/`

### Events related
Endpoints for viewing neatby events.

* [Show Nearby Events](events/get.md) : `GET /api/events/`
* [Create Event](events/post.md) : `POST /api/events/`
