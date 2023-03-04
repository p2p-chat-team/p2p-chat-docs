# p2p-chat
The p2p-chat application provides a peer-to-peer chat service.

## Repo's
This project is split over multiple repositories:
- [p2p-chat-server](https://github.com/p2p-chat-team/p2p-chat-server): a flask API which is basically one giant contact list (username - ip)
- [p2p-chat-terminal-client](https://github.com/p2p-chat-team/p2p-chat-terminal-client): a cli application that uses socket connections to chat peer-to-peer
- [p2p-chat-common](): holds all tools to manage application + repo's. makefile(s), docker, etc...
- [p2p-chat-docs](https://github.com/p2p-chat-team/p2p-chat-docs): holds documentation on the full application and all repo's

## Infrastructure
The documentation on the infrastructure of this application is provided in a [separate file](docs/infrastructure.md)