# A simple MERN(MONGODB, EXPRESSJS, REACTJS & NODEJS) stack application 

## Switch to the master branch to see the automation of this App using github actions.

### Create a network for the docker containers

`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t frontend .
```

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongodb:latest`

### Build the server

```sh
cd mern/backend
docker build -t backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 backend`

## Using Docker Compose

`docker compose up -d`

Then confirm if its working at 'http://localhost:5173'
  
![Image](https://github.com/user-attachments/assets/14bf7d82-0203-4453-8eea-e48c4ff15035)

To shut it down use ' docker compose down '

