# server

[![Build Status](https://travis-ci.org/lucasOlivio/showcase/server/server.svg?branch=master)](https://travis-ci.org/lucasOlivio/showcase)
[![Built with](https://img.shields.io/badge/Built_with-Cookiecutter_Django_Rest-F7B633.svg)](https://github.com/agconti/cookiecutter-django-rest)

Simple showcase page for small business. Check out the project's [documentation](http://lucasOlivio.github.io/showcase/).

# Prerequisites

- [Docker](https://docs.docker.com/docker-for-mac/install/)  

# Local Development

Start the dev server for local development:
```bash
docker-compose up
```

Run a command inside the docker container:

```bash
docker-compose run --rm web [command]
```
