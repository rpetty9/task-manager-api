# task-manager-api
Project to showcase my API project


# Task Manager API

## Overview

- The Task Manager API is a RESTful API that allows users to manage tasks efficiently. Users can create, read, update, and delete tasks while leveraging authentication for secure access. This project is designed to demonstrate API development with Flask/FastAPI, database integration, and authentication.

## Tech Stack


| Categories       | Technologies           |
| ------------- |:-------------:|
| Backend      | Flask/FastAPI (Python) |
| Database      | SQLite / PostgreSQL (SQLAlchemy for ORM)|
| Authentication | JWT (JSON Web Token)   |
| Documentation      | Swagger UI / Postman |
| Deployment      | Render, Railway, or AWS Lambda |


## Features

- User Authentication: Register/Login users and issue JWT tokens.

- Task CRUD Operations: Create, read, update, and delete tasks.

- Filtering & Sorting: Retrieve tasks by status and sort by due date.

- API Documentation: Swagger UI (for FastAPI) or a Postman collection.

## Installation & Setup

### Prerequisites

- Python 3.8+

- Virtual environment (optional but recommended)

### Setup Instructions

1. Clone the repository:

git clone https://github.com/yourusername/task-manager-api.git
cd task-manager-api

2. Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

3. Install dependencies:

pip install -r requirements.txt

4. Set up environment variables: (Create a .env file)

SECRET_KEY=your_secret_key_here
DATABASE_URL=sqlite:///tasks.db

5. Run database migrations (if applicable):

python migrate.py  # Flask
alembic upgrade head  # FastAPI (if using Alembic)

6. Run the API server:

python app.py  # Flask
uvicorn main:app --reload  # FastAPI

## API Endpoints

| Method        |  Endpoint         | Description  |
| ------------- |-------------| :-----:|
| POST     | /register | Register a new user |
| POST      | /login      |   Authenticate and get a token |
| GET | /tasks     |  Retrieve all tasks |
| POST     | /tasks | Create a new task |
| GET      | /tasks/{id}      |   Get task details by ID |
| PUT | /tasks/{id}      |    Update task details |
| DELETE | /tasks/{id}     |    Delete a task |


## Authentication

- Users must include a JWT token in the Authorization header for protected routes.

- Example request with a token:

curl -H "Authorization: Bearer your_token_here" http://localhost:8000/tasks

## Testing with Postman

1. Import the provided Postman collection (link or JSON file in the repo).

2. Set up authentication and test CRUD operations.

## Deployment (Optional)

To deploy the API:

- Use Render, Railway, or AWS Lambda for server hosting.

- Use PostgreSQL as a production database.

- Configure CI/CD pipelines for automated deployment.

## Future Enhancements

- Implement OAuth authentication (Google/GitHub login).

- Add task categories & priorities.

- Develop a frontend UI using React or Vue.js.

## License

- This project is licensed under the MIT License. Feel free to use and modify it.


## Dictionary

### API

- An API is a set of rules that allow different software applications to communicate. It defines endpoints (URLs), methods (GET, POST, PUT, DELETE), and data formats (JSON, XML).
- An API is a bridge that allows different applications to talk to each other.:

#####  Real-World Analogy:
Think of an API like a waiter in a restaurant:

1. You (the client) order food (request data).
2. The waiter (API) takes your order to the kitchen (server).
3. The kitchen prepares the food (processes the request).
4. The waiter brings the food back to you (response).
