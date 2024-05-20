# LAMP Stack (docker-compose)

## Overview

This is the starter code for a LAMP Stack. The docker-compose.yml file is missing and should be
created. Please check the following sections for more details about how to get started and for
instructions to build the docker-compose.yml file.

## Getting Started

```bash
# Clone the project
git clone https://github.com/EdgeKing810/interns-docker-compose-lamp.git
cd interns-docker-compose-lamp/
```

Please make sure that you have docker installed on your system before continuing.

## Instructions

1. Rename the `.env.sample` file to `.env` and **add the required variables**.
2. Modify `bin/webserver/Dockerfile` and resolve the comment on line 23.
3. Create the `docker-compose.yml` file.
4. Add a service that uses `bin/webserver/Dockerfile` named webserver, which maps the
`./webroot`, `./config/php/php.ini`, `./config/vhosts` and `./logs/apache2` directories
and files as volumes at the correct paths inside of the container. A port mapping should
also be done that uses the `HOST_MACHINE_HTTP_PORT` variable.
6. Add a service based on the `DB_SERVER` variable defined in the `.env` file that
does a port mapping based on the `HOST_MACHINE_MYSQL_PORT` variable. The variables
added during step 1 need to be added to this service. The `./data/mysql` and `./logs/mysql`
directories should also be mapped as volumes at the correct paths inside of the container.
7. Add a final service for `phpmyadmin`, which does a port mapping related to the
`HOST_MACHINE_PHPMYADMIN_PORT` variable and which uses the variables added during step 1.
8. Start the containers with the `docker compose up` command, check the logs, check if
the mounted volumes have been mapped correctly and troubleshoot if necessary. Fix any
errors that might show up on the interfaces of services deployed.
