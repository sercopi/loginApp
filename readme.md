### Deploy

run on the host machine the following command on the root folder of the project:
docker-compose up --scale api-server=3 && cd ./frontend/simple-vue-app && npm i && npm run serve

### definition
A project to simmulate the flow of a client application managing user registration: singing up/registering/retrieving forgotten passwords using the openID connect protocol.

THE FLOW: An Auth server (Auth API) logs and stores user credentials through a client (a simple VUE app). The authentication server, acting as an identity provider, issues valid JsonWebTokens that the client passes to a simple API to authenticate. The API, acting as a normal backend that doesn´t store credentials, authenticate the tokens against the authServer and provides the needed service to the client.

THE GOAL: The goal for this project was to fully understand and recreate a modern login/registration flow using an external identity provider (similar to using Google, Apple or Facebook login) AND to learn different technologies in the process! There is a backend that manages messaging asynchronously using rabbitMQ, and a non relational DB that uses mongoDB, all deployed in different docker containers, and distributed through an Nginx server, where I´m also trying its load balancing capabilities (that´s why the Auth API is recreated with 3 containers) :D!

IN THE FUTURE, COMING IN ANGULAR!
