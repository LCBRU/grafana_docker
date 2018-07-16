# Grafana Docker Container

This repository defines a container for running the Grafana reporting
tool.

## To Run

To produce a working environment make the following amendments:

1. Take a copy of the file `example.env` called `.env`.
2. In the `.env` file, change the value of the `GF_SECURITY_ADMIN_PASSWORD`
environment vaiable from `{password}` to a strong password.
3. Take a copy of the file `example.ldap.toml` called `ldap.toml`.
4. In the `ldap.toml` file, change the value of the `host` variable
from `{LDAP SERVER HOST NAME}` to the host name of the LDAP server.
5. Start the container by running the command `docker-compose up`

## Persistent Storage

To allow the changes made to the data sources, dashboards and users
to be persisted between instances of the Docker container, the
persistent data is saved in the `./persisitent` directory.

In order for the container to write to the `./persistent` directory,
you will need to amend the permissions on the directory to allow the
user that runs Docker to write to it.

To clear out the saved data, delete all the content from the `./persistent`
directory.