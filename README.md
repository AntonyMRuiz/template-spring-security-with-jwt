##docker-compose (Docker-swang) - orquestador

services:

app:
build: .
container_name: template-docker
ports:
- "8085:8080"
depends_on:
- db

db:
image: mysql:8.0
container_name: mysql-docker-db
ports:
- "3308:3306"
volumes:
- db_data:/var/lib/mysql

volumes:
db_data:

