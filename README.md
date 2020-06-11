# Antidot Framework - Development server

## Packages

* PHP 7.4.3
* Redis
* Nginx Server

## Requirements

* [docker](https://docs.docker.com/install/)
* [docker-compose](https://docs.docker.com/compose/install/)

## Installation

### Docker

```bash
git clone git@github.com:antidot-framework/docker-dev-server.git your-project
cd your-project
rm -rf .git
./install.sh
```

## Usage

### Run App

````bash
docker-compose up -d
````
Open it on [localhost](http://localhost).
