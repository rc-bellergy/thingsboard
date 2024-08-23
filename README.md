# Notes: How to start the frontend development server.

## GitHub
    https://github.com/rc-bellergy/thingsboard.git
    https://github.com/swimlane/ngx-ui

## Fail to connect oauth2Clients
 - Start the local thingsboard server on 8080 port for login
 - update the server address in the proxy.conf.js file

## Install
    yarn install

- nodeVersion: v20.11.1
- yarnVersion: v1.22.17

## Start

    npm run start

## Custom theme style

    /src/theme.scss

## Build UI-NGX

    npm run build:prod

## Build updated docker image using Maven

    mvn clean install -DskipTests -Ddockerfile.skip=false

## Upload to Docker Hub

    docker tag thingsboard/tb-postgres:latest bellergy/tb-postgres:latest
    docker push bellergy/tb-postgres:latest 

## Load new docker image

  1. Check the docker-compose.yml. The image should use bellergy/tb-postgres:latest
  2. docker compose up --build -d
  3. docker compose logs -f mytb



