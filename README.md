docker-storj
============

An easy to use wrapper for running a storj network locally.

> Note: This repo is in a very early state, YMMV

# Usage

```sh
git clone --recursive git@github.com:retrohacker/docker-storj
cd docker-storj
docker-compose build
docker-compose up
```

# Advantages

Since each repo is broken out into a gitsubmodule in this project, and each repo gets it's own Dockerfile, you wont need to rebuild the entire project for every code change. In fact, a majority of the time you `docker-compose build` will only need to add your code changes into the docker-image taking less than 5 seconds for a build.

This also lets you try to scale out infrastructure. `docker-compose scale farmer=10` will scale out a federation of farmers for you. Finally, since we are building Docker images for each repo and bind-mounting state into the running container, you can use your local development environment when working on this project.

🍻
