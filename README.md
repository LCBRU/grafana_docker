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
5. Build the container by running the command `docker-compose build`
6. Start the container by running the command `docker-compose up`
