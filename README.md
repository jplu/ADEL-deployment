# ADEL-deployment
Kubernetes, Helm and Docker compose scripts for deploying ADEL

# Requirements
* `sudo sysctl -w vm.max_map_count=262144` (more details [here](https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html))
* `export DOCKER_CLIENT_TIMEOUT=120`
* `export COMPOSE_HTTP_TIMEOUT=120`

To properly run ADEL you have to have at least 10 GB of RAM and 60 GB of disk space fully dedicated to ADEL.

# Start ADEL
To start ADEL with Docker compose, run the following command line:

```docker-compose up -d```

Be sure to be in the `docker-compose` folder to run this command. Once all the images have been downloaded, wait 5 minutes to be sure that everything is properly set. Be careful, the Docker image for the index is around 50GB to download so be sure to have a proper internet connection.
