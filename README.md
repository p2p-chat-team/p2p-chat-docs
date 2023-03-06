# p2p-chat
The p2p-chat application provides a peer-to-peer chat service.

## Repo's
This project is split over multiple repositories:
- [p2p-chat-server](https://github.com/p2p-chat-team/p2p-chat-server): a flask API which is basically one giant contact list (username - ip)
- [p2p-chat-terminal-client](https://github.com/p2p-chat-team/p2p-chat-terminal-client): a cli application that uses socket connections to chat peer-to-peer
- [p2p-chat-common](): holds all tools to manage application + repo's. makefile(s), docker, etc...
- [p2p-chat-docs](https://github.com/p2p-chat-team/p2p-chat-docs): holds documentation on the full application and all repo's

## Features
### Server
As this chat application works peer-to-peer, there's no need for a server that handles the chatting. 
This server is basically a client contact list, so people can just share their usernames, and their ips can be fetched from this server. <br>
That's why only these features are needed:
- **Register**: A client should be able to register themselves in the client list. A username, password and a host-ip are required.
- **Fetch client list**: A client should be able to fetch a list of all clients
- **Fetch one client**: A client should be able to fetch information about a single client by their username
- **Unregister**: A client should be able to remove themselves from the client list. Their password is required for safety.

A more detailed look in the features of the server can be found in the [API documentation](docs/api_documentation.md)

### Terminal client
The cli client for this peer-to-peer chat application has the following functionality.
- **Register**: Send a request to the server to register your client by username.
- **Fetch clients**: Display all registered clients who are registered as a contact list.
- **Manual connect**: Start a chat with another client, by manually providing an ip-address to connect to.
- **Connect with username**: Start a chat with another client, by providing their username. Their ip-address to connect will be fetched from the server.

## Infrastructure
The documentation on the infrastructure of this application is provided in a [separate file](docs/infrastructure.md)
