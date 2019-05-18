# Antidot Framework - Development server

## Packages

* PHP 7.3.5
* Redis
* Nginx Server

## Requirements

* docker
* docker-compose

## Installation

````bash
git clone git@github.com:antidot-framework/docker-dev-server.git
cd docker-dev-server
composer create-project antidot-fw/antidot-framework-starter:dev-master ${PWD}/app
````

## Usage

### Run App

````bash
docker-compose up --build -d
````
