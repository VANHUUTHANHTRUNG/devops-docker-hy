# Docker Nodejs Express Mongo Demo #
This demo was used to practice and learn Docker with Nodejs and Mongo
Mongo Express was used for database managing an monitoring in a more UI-wise manner
Containers for nodejs app, database and mongo-express were setup with some additional
parameters.
The application is simple yet sufficient to try putting together these tech and
orchestrate with docker-compose

# To start #
- `docker-compose up`
- Access the database UI monitoring via `localhost:8080`
- It is possible to create database and collection in mongodb via both CLI inside
the container accessed via `docker exec -it <mongodb_container>` and the web interface
- Nodejs application is available at `localhost:3000` for interacting

