# OMERO.server and OMERO.web (docker-compose)

## Custom Server
First, build the custom server image.

    docker build ./CUSTOM-SERVER -t omero-server:custom

The custom server build includes the script and dependencies to create PDFs for OMERO.figure.

## Run

Set the `DB_VOLUME` and `OMERO_VOLUME` variables in the environment file 
(`.env`).

    docker-compose up -d
    docker-compose logs -f
