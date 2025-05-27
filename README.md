# A simple MERN(MONGODB, EXPRESSJS, REACTJS & NODEJS) stack application 

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

- ![Screenshot 2023-02-01 at 5 46 14 PM]("C:\Users\Azeez2\Pictures\Screenshots\mern.png")https://github.com/Omokehinde-hub/MERN-APP/issues/1#issue-3094405376
- 
