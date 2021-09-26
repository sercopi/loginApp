###Deploy

run on the host machine the following command on the root folder of the project:
docker-compose up --scale api-server=3 && cd ./frontend/simple-vue-app && npm i && npm run serve

