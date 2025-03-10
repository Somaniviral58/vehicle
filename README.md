Vehicle Management API

Overview

The Vehicle Management API is a Spring Boot-based RESTful web service that allows users to create, update, retrieve, and delete vehicle records.

Features

Create a new vehicle

Update an existing vehicle

Retrieve all vehicles

Delete a vehicle by ID

Technologies Used

Java 17

Spring Boot

Spring Data JPA

Hibernate

Lombok

PostgreSQL/MySQL (or any relational database)

Postman (for API testing)

Installation and Setup

Prerequisites

Java Development Kit (JDK 17 or later)

Maven

PostgreSQL/MySQL Database

An API testing tool like Postman

Clone the Repository

$ git clone https://github.com/your-repo/vehicle-management.git
$ cd vehicle-management

Configure Database

Update application.properties in src/main/resources with your database configuration:

spring.datasource.url=jdbc:mysql://localhost:3306/vehicle_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update

Build and Run the Application

$ mvn clean install
$ mvn spring-boot:run

API Endpoints

Create a Vehicle

POST /api/vehicles/createvehicle

{
  "vehicleRegistrationNumber": "ABC123",
  "ownerName": "John Doe",
  "brand": "Toyota",
  "registrationExpires": "2025-12-31T00:00:00",
  "isActive": true,
  "createdBy": "admin"
}

Update a Vehicle

PUT /api/vehicles/updatevehicle

{
  "id": 1,
  "vehicleRegistrationNumber": "ABC123",
  "ownerName": "John Doe Updated",
  "brand": "Honda",
  "registrationExpires": "2026-12-31T00:00:00",
  "isActive": true,
  "modifiedBy": "admin"
}

Retrieve All Vehicles

GET /api/vehicles/all

Delete a Vehicle by ID

DELETE /api/vehicles/deletevehicle/{id}

Error Handling

400 Bad Request: Validation errors

404 Not Found: Vehicle not found

500 Internal Server Error: Unexpected server issues

License

This project is licensed under the MIT License.
