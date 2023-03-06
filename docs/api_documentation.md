# p2p-chat server API
The server has an API to access its features. 
Here more information on all the endpoints which can be used, and how a request to them should look. 

## Endpoints

### Fetch the client list
`GET /clients`

#### Parameters

| Type | Name | Description | Schema |
|------|------|-------------|--------|
|      |      |             |        |

### Fetch a client by username
`GET /clients/{username}`

| Type | Name                       | Description | Schema |
|------|----------------------------|-------------|--------|
| Path | **username**<br/>_require_ |             | string |

### Register a new client
`POST /register`

#### Parameters
| Type | Name                        | Description              | Schema |
|------|-----------------------------|--------------------------|--------|
| Body | **username**<br/>_required_ |                          | string |
| Body | **password**<br/>_required_ |                          | string |
| Body | **host**<br/>_required_     | Ip-address of the client | string |

### Un-register a client
`DELETE /clients/{username}`

Remove an existing client from the client list. This is protected by a password.

#### Parameters
| Type | Name                        | Description | Schema |
|------|-----------------------------|-------------|--------|
| Path | **username**<br/>_required_ |             | string |
| Body | **password**<br/>_required_ |             | string |