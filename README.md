# Campus Taskboard API

## Project Description

This project is a Spring Boot REST API that allows users to manage tasks. Users can create, read, update, and delete tasks (CRUD operations). The API also includes input validation to ensure that all data entered meets requirements such as title length and required fields.

This project demonstrates how to build a structured backend using controllers, services, and models in Spring Boot.

The application follows a layered architecture:
- Controller: Handles HTTP requests
- Service: Contains business logic
- Model: Represents task data
---

## How to Run the Application

### Option 1: Using an IDE

1. Open the project in IntelliJ IDEA or VS Code
2. Locate `CampusTaskboardApplication.java`
3. Right-click and click **Run**
4. The server will start at:
   [http://localhost:8080](http://localhost:8080)

### Option 2: Using Terminal

1. Open a terminal in the project folder
2. Run:
   ./mvnw spring-boot:run
3. Open in browser or Postman:
   [http://localhost:8080/api/tasks](http://localhost:8080/api/tasks)

---

## API Endpoints Documentation

## Testing the API

The API was tested using Postman.

Each endpoint (GET, POST, PUT, DELETE) was tested by sending HTTP requests to:
http://localhost:8080/api/tasks

Headers used:
Content-Type: application/json

Screenshots of successful requests and responses are included in the project submission.

### GET all tasks

###GET /api/tasks
Returns a list of all tasks

---

### GET task by ID

GET /api/tasks/{id}
Returns a single task by ID

---

### POST create task

POST /api/tasks
Creates a new task

Example JSON:
{
   "title": "Complete Homework 5",
   "description": "Finish Spring Boot API assignment",
   "completed": false,
   "priority": "HIGH"
}

---

### PUT update task

PUT /api/tasks/{id}
Updates an existing task

Example JSON:
{
   "title": "Updated Task",
   "description": "Updated description",
   "completed": true,
   "priority": "HIGH"
}

---

### DELETE task

DELETE /api/tasks/{id}
Deletes a task

---

## Validation

The API validates input using Spring Validation:

* Title must be between 3 and 100 characters
* Title cannot be empty
* Description cannot exceed 500 characters

If invalid data is submitted, the API returns a 400 Bad Request with error messages.

---

## Video Link

(Paste your video link here)

---

# -Creating-Your-First-Spring-Boot-API-with-Validation
