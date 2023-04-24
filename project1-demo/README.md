# Webinar Demo Project 1

## Enable

First, make sure your working directory is `project1-demo`.

To bring up the solution:

    docker-compose up -d

## Connect

Once the solution has been launched, you can begin to access the services at:

- Frontend Ignition Gateway - http://frontend1.localtest.me
- Backend Ignition Gateway - http://backend1.localtest.me

Default admin credentials for Ignition Gateways are `admin` / `password`. Default credentials for PostgreSQL DB are `ignition` / `ignition`.

## Monitor

If you'd like to monitor the logs of any of the services, you can use the following:

    docker-compose logs --tail=250 -f <service name>

... where `<service name>` is one of the named services from `docker-compose.yml`, e.g. `gateway` or `db`.  Omit the `<service name>` to start viewing logs from all services.  Use `CTRL-C` to break out of the log view.

## Shutdown

To shutdown the containers within the solution:

    docker-compose down

Note that this will leave data volumes intact on your system so that bringing the solution back online will return to the previous state.  If you want to also remove the data volumes and return the solution to the original state, add a `-v` flag to the *down* command.
