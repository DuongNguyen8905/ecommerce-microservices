# Spring Boot E-commerce Microservices

This repository demonstrates the migration of an e-commerce application from a monolithic architecture to a microservices architecture.

## Project Structure

- springboot-ecommerce/ : Original monolithic application
- user/ : User Service
- product/ : Product Service
- order/ : Order Service
- docker-compose.yml : PostgreSQL & pgAdmin setup

## Technologies

- Java 21
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Docker
- Docker Compose

  
##  Running the Project

1. Clone the repository

git clone git@github.com:DuongNguyen8905/ecommerce-microservices.git

cd ecommerce-microservices/springboot-ecommerce

3. Start PostgreSQL
   
docker compose up -d

Make sure PostgreSQL is running before starting the Spring Boot application.

5. Create the database
   
If the database does not already exist, create:  ecomdb

docker exec -it postgres_container psql -U duong

Then:   CREATE DATABASE ecomdb;

Exit PostgreSQL 

7. Run the Spring Boot application
   
On Linux/macOS:    ./mvnw spring-boot:run

On Windows:     mvnw.cmd spring-boot:run

The application will start on the port configured in application.properties or application.yml.
