# Sample Spring Boot Application

## Overview
This project is a small web service that utilizes the following technologies:

* Java 9
* Spring MVC with Spring Boot
* Maven

## Architecture
The architecture of the web service is built with the following components:

Data Transfer Objects (DTOs): Objects used for external communication via the API.
Controller: Implements the processing logic of the web service, including parameter parsing and input/output validation.
Service: Implements the business logic and handles the access to the Data Access Objects.
Data Access Objects (DAOs): Interface for the database, handling the insertion, updating, deletion, and retrieval of objects.
Domain Objects: Functional objects that may be persisted in the database.

## Getting Started
You can start the example application by executing the com.myapp.MyappServer class, which will start a web server on port 8080 (http://localhost:8080) and serve the Swagger UI, where you can inspect and try the existing endpoints.

## Useful commands
Here are some sample curl commands that you can use to test the application:

```
# Get all cars
curl -u user:password "http://localhost:8080/v1/cars"

# Get online drivers
curl -u user:password "http://localhost:8080/v1/drivers?onlineStatus=ONLINE"

# Get non-deleted online drivers
curl -u user:password "http://localhost:8080/v1/drivers?onlineStatus=ONLINE&deleted=false"

# Get non-deleted online driver with username "driver01"
curl -u user:password "http://localhost:8080/v1/drivers?onlineStatus=ONLINE&deleted=false&username=driver01"

# Update a driver's car
curl -u user:password -X PUT "http://localhost:8080/v1/drivers/4/car/4545PWR"
```
You can also test the application using the Swagger UI available at http://localhost:8080/swagger-ui.html.