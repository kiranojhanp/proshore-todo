# Todo app assignment for proshore

## Technologies used

- Backend: NodeJS, Typescript, Mongoose, Docker
- Frontend: React, Redux toolkit, Typescript, TailwindCSS

## Introduction

- This repo basically contains two repos (frontend and backend) as submodules.
- The usage of git submodules helps with the proper seperation of frontend and backend developement.
- both repos contain individual `Dockerfiles`
- The `docker-compose.yml` in the runs them

## Expected result

The expected outcome is to be able to serve the application with the command `docker-compose up`

## Problem

There is a problem with create-react-app and docker which results to a build fail at the moment. I have been trying different solutions but haven't figured out the solution yet.

## Solution

For the time being, I have set up a script that runs backend and frontend in parallel without the need of `Docker`. The `Dockerfile` and `docker-compose.yml` do not serve any purpose currently. I will update the repo after I find the fix.

## Steps to run the application

### Run mongodb

1. Start mongodb from your desired location. I use `mongod --dbpath ~/data/db`

### clone the repo and fetch submodules

1. `cd Desktop`
2. `git clone https://github.com/kiranojhanp/proshore-todo`
3. `cd proshore-todo`
4. `git submodule update --init --recursive`
5. `git submodule update --recursive --remote`

### start the application

1. `npm start`
