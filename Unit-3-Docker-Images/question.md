# question 1

a company wants to deploy a 3-tier web app using docker compose: 
frontend-> react
backend->spring boot api
database-> postgresql
requirements:
all services must communicate
- environment variables should be used
- data should persist using volumes
- services must start in dependency order 



# question 2

Deploy a WordPress website using Docker Compose with MySQL as the database.Requirements:
WordPress runs on port 8080 
MySQL uses persistent storage 
Use environment variables for DB configuration 
Ensure proper service dependency


# question2 compose file
version: '3.8'

services:
  wordpress:
    image: wordpress:latest
    container_name: wordpress-app
    ports:
      - "8080:80"
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wpuser
      WORDPRESS_DB_PASSWORD: wppass
      WORDPRESS_DB_NAME: wpdb
    depends_on:
      - db

  db:
    image: mysql:5.7
    container_name: mysql-db
    restart: always
    environment:
      MYSQL_DATABASE: wpdb
      MYSQL_USER: wpuser
      MYSQL_PASSWORD: wppass
      MYSQL_ROOT_PASSWORD: rootpass
    volumes:
      - db-data:/var/lib/mysql

volumes:
  db-data:



  ********************o--------------------********************


# question3
create a docker compose setup for a node.js app connected to MongoDB.
Requirements:
Node.js app runs on port 3000
MongoDB runs on default port 27017
Use environment variables for DB connnection
Ensure MongoDB starts before Node.js
