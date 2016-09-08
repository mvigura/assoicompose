# ASSOI Compose

## Prerequisites
- git
- [Docker](https://docs.docker.com/engine/installation/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Installation
1. ```cd /path/to/working/directory```
1. ```git clone --recursive https://github.com/qwemaze/assoicompose.git```

## Import db
1. ```cd /path/to/assoicompose```
1. ```sudo docker-compose down```
1. remove contents of ```postgres/data/```
1. remove contents of ```mongo/data/```
1. copy dump file to ```postgres/assoi.dump```
1. ```sudo docker-compose up -d assoi-postgres assoi-mongo```
1. ```sudo docker-compose exec assoi-postgres /bin/bash -c '/var/lib/postgresql/import.sh'```
1. ```sudo docker-compose run -w /www assoi /bin/bash -c 'npm i && node install.js'```
1. ```sudo docker-compose down```

## Up
1. ```cd /path/to/assoicompose```
1. ```sudo docker-compose up -d```

## HALPH
- ```sudo docker-compose --help```
- ```sudo docker --help```
- Google
- [Dmitriy Kovyazin](mailto:dkoviazin@gmail.com) (```ugmk/``` submodule)
- [Elias Baryshnikov](mailto:qwelias@gmail.com)
