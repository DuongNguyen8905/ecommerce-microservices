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

2. Start PostgreSQL
   
docker compose up -d

Make sure PostgreSQL is running before starting the Spring Boot application.

3. Create the database
   
docker exec -it postgres_container psql -U duong -c "CREATE DATABASE ecomdb;"
 

4. Run the Spring Boot application
   
On Linux/macOS:    ./mvnw spring-boot:run

On Windows:     mvnw.cmd spring-boot:run

The application will start on the port configured in application.properties or application.yml.

## API Testing

The APIs can also be tested using Postman.

Example CRUD operations:

POST   /api/users
GET    /api/users
GET    /api/users/{id}
PUT    /api/users/{id}

POST   /api/products
GET    /api/products
GET    /api/products/{id}
GET    /api/products/search?keyword=ip
PUT    /api/products/{id}
DELETE /api/products/{id}

POST   /api/cart
DELETE /api/cart/items/1
GET    /api/cart

POST   /api/orders

## Project Goals

Refactor a monolithic Spring Boot application into scalable, independent microservices.

Design and build robust RESTful CRUD APIs.

Integrate PostgreSQL integrated with Spring Data JPA/Hibernate.

Integrate Docker Compose.

Document and test APIs via Postman.
