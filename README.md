# Todo app assignment for proshore

## Technologies used

- Backend: NodeJS, Typescript, Mongoose, Redis, Docker
- Frontend: React, Redux toolkit, Typescript, TailwindCSS

## Introduction

- This repo basically contains two repos (frontend and backend) as submodules.
- The usage of git submodules helps with the proper seperation of frontend and backend developement.
- both repos contain individual `Dockerfiles`
- The `docker-compose.yml` in the runs them
- Majority of the code is self explainatory. Comments are added in few tricky parts.

## Expected result

The expected outcome was to be able to serve the todo application with the command `docker-compose up`.

## Problem occured

There is a problem with create-react-app and docker which results to a build fail at the moment. I have been trying different solutions but haven't figured out the solution yet.

## Solution

For the time being, I have set up a script that runs backend and frontend in parallel without the need of `Docker`. The `Dockerfile` and `docker-compose.yml` do not serve any purpose (except for viewing) currently. I will update the repo so it used docker after I find the fix.

## Steps to run the application

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
