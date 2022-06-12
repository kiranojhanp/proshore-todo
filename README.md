# Todo app assignment for proshore

## Technologies used

- Backend: NodeJS, Typescript, Mongoose, Redis, Docker
- Frontend: React, Redux toolkit, Typescript, TailwindCSS

## Introduction

- This repo basically contains two repos (frontend and backend) as submodules.
- The usage of git submodules helps with the proper seperation of frontend and backend developement.
- both repos contain individual `Dockerfiles`
- The `docker-compose.yml` in this repo runs them in a same container
- Majority of the code is self explainatory. Comments are added in few tricky parts.

## How to use

There are two ways to run the application.

### Using docker
- `docker compose up` on the root 

### Using npm
- `npm start` on the root


## Steps to run the application

### Using docker?
No need to do anything the `docker compose up` takes care of everything

### USing mongodb

### Run mongodb

1. Install mongodb from [mongodb installation page](https://www.mongodb.com/try/download/community)
2. Start mongodb from your desired location. I use `mongod --dbpath ~/data/db`.

### Run redis

1. Start redis.

- Install redis from [redis installation page](https://redis.io/docs/getting-started/installation/)
- Run the redis according to above page. I use `brew services start redis`.

### clone the repo and fetch submodules

1. `cd Desktop`
2. `git clone https://github.com/kiranojhanp/proshore-todo`
3. `cd proshore-todo`
4. `git submodule update --init --recursive`
5. `git submodule update --recursive --remote`

### start the application

1. `npm start`
