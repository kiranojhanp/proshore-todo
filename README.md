## Introduction
- This repo basically contains two repos (frontend and backend) as submodules.
- The usage of git submodules helps with the proper seperation of frontend and backend developement.
- both repo contain individual `Dockerfiles`
- The `docker-compose.yml` in the runs them

## Expected result
The expected outcome is to be able to serve the application with the comman `docker-compose up`

## Problem
There is a problem with create-react-app and docker which results to a build fail at the moment. I have been trying different solutions but haven't figured out the solution yet. So, For the time being, I recommend cloning both `backend` and `frontend` repos.

## Steps to run the application

### clone the repo and fetch submodules
1. `cd Desktop`
2. `git clone https://github.com/kiranojhanp/proshore-todo`
2. `cd proshore-todo`
3. `git submodule update --init --recursive`
4. `git submodule update --recursive --remote`

### install dependencies
1. `cd todo-backend && npm install && cd ..`
2. `cd todo-frontend && npm install && cd ..`

### Run mongodb
1. Start mongodb from your desired location. I use `mongod --dbpath ~/data/db`

### Run both frontend and backend
- Open two terminals and run these simultaneously
1. `cd todo-backend && npm start`
2. `cd todo-frontend && npm start`
