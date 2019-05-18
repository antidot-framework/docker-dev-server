# Antidot Framework - Development server

## Packages

* PHP 7.3.5
* Redis
* Nginx Server

## Requirements

* [docker]()
* [docker-compose]()

## Installation

### Docker

````bash
git clone git@github.com:antidot-framework/docker-dev-server.git
cd docker-dev-server
composer create-project antidot-fw/antidot-framework-starter:dev-master ${PWD}/app
````

### Docker Machine

#### Requirements

* [Docker machine]()
* [Virtualbox]()

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
