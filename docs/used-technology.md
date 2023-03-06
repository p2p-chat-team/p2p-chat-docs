# Used technology
In this document you can find more information about all the technologies used in this application.

## Server
The server is an API, which uses the python framework [flask](https://palletsprojects.com/p/flask/).

### Database
To save all the clients, there has to be a database. A `sql` database can be configured for the server, 
using [sqlalchemy](https://flask-sqlalchemy.palletsprojects.com/en/3.0.x/) for the database connection. 

#### Migrations
[flask-migrate](https://flask-migrate.readthedocs.io/en/latest/) will be responsible for managing the migrations to the database. 
Here a quick rundown on how to initialize the database, etc...

**Initialize database**: `flask db init`

**Generate a migration**: `flask db migrate -m "migration message"`

**Upgrading to the latest migration**: `flask db upgrade`

If there is anything else you need from `flask-migrate` you can run following help command: `flask db --help`

## Terminal-client
This client is a cli application, using the python library [typer](https://typer.tiangolo.com/) for handling the commands.

To handle the peer-to-peer connections, the built-in python library [socker](https://docs.python.org/3/library/socket.html) will be used. 