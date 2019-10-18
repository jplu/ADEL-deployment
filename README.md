# ADEL-deployment
Kubernetes, Helm and Docker compose scripts for deploying ADEL

# Requirements
* `sudo sysctl -w vm.max_map_count=262144` (more details [here](https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html))
* `export DOCKER_CLIENT_TIMEOUT=120`
* `export COMPOSE_HTTP_TIMEOUT=120`
* [FR-EN pipeline](docker-compose/docker-compose.yaml): requires at least 14 GB of RAM and 70 GB of disk space fully dedicated to ADEL.
* [FR pipeline](docker-compose/docker-compose-fr.yaml):  requires at least X GB of RAM and X GB of disk space fully dedicated to ADEL.
* [EN pipeline](docker-compose/docker-compose-en.yaml): requires at least X GB of RAM and X GB of disk space fully dedicated to ADEL.

# Docker compose
Be careful, the Docker image for each index is around 50GB to download so be sure to have a proper internet connection. Once all the images have been downloaded, wait 10 minutes to be sure that everything is properly set.

## FR-EN pipeline
To start this pipeline with Docker compose, run the following command line:

```docker-compose up -d```

## FR pipeline
To start this pipeline with Docker compose, run the following command line:

```docker-compose -f docker-compose-fr.yaml up -d```

## EN pipeline
To start this pipeline with Docker compose, run the following command line:

```docker-compose -f docker-compose-en.yaml up -d```
