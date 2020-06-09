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

````bash
git clone git@github.com:antidot-framework/docker-dev-server.git
cd docker-dev-server
composer create-project antidot-fw/antidot-framework-starter ${PWD}/app
````

### Docker Machine

#### Requirements

* [Docker machine](https://docs.docker.com/machine/install-machine/)
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)

````bash
git clone git@github.com:antidot-framework/docker-dev-server.git
cd docker-dev-server
composer create-project antidot-fw/antidot-framework-starter:dev-master ${PWD}/app
docker-machine create --driver virtualbox [machine-name] 
docker-machine stop [machine-name]
vboxmanage sharedfolder add [machine-name] --name "app" --hostpath "${PWD}/app"
docker-machine start [machine-name]
eval "$(docker-machine env [machine-name])"                                             
````

## Usage

### Run App

````bash
docker-compose up --build -d
````
Open it on [localhost](http://localhost).
