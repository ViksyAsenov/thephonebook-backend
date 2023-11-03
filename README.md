# Phonebook Backend App

This is a simple Node.js application for managing a [phonebook](https://thephonebook-backend.onrender.com). It provides a RESTful API to perform basic CRUD operations on a list of people. This application uses Express.js for the server, MongoDB as the database, and includes error handling with validation. Additionally, it uses the `dotenv` library for managing environment variables and `morgan` for logging requests.

## Features

- List all people in the phonebook.
- Retrieve a single person's information by ID.
- Add a new person to the phonebook.
- Update an existing person's information.
- Delete a person from the phonebook.
- Get information about the number of people in the phonebook and server status.

## Prerequisites

Before you begin, ensure you have the following software and resources:

- Node.js
- MongoDB (accessible online)
- Git (for cloning the repository)

### Installation

1. **Clone the Repository:**
   :
     ```
     git clone https://github.com/ViksyAsenov/thephonebook-backend
     ```

2. **Navigate to the project directory:**
   :
     ```
     cd thephonebook-backend
     ```

3. **Install the required dependencies:**
   :
     ```
     npm install
     ```

4. **Create a `.env` file in the root directory and define the following environment variables:**
   :
```
PORT=3001 # Port on which the server will run
MONGODB_URI=your-online-mongodb-connection-string
```

## API Endpoints

- `GET /api/persons`: Get a list of all people in the phonebook.
- `GET /api/persons/:id`: Get the information of a person by their ID.
- `POST /api/persons`: Add a new person to the phonebook.
- `PUT /api/persons/:id`: Update the information of an existing person.
- `DELETE /api/persons/:id`: Delete a person from the phonebook.
- `GET /info`: Get information about the phonebook, including the number of people and server status.

## Logging

This application uses `morgan` for request logging. Request logs are displayed in the console and include the HTTP method, URL, response status, content length, response time, and the request body (for POST requests).

## Frontend Integration
The frontend build is served using Express's static file serving. You can access the frontend by visiting `http://localhost:PORT` in your browser. Ensure that your frontend build is in a folder named `build` within your project directory.

## Error Handling

The application handles errors and provides appropriate responses for various error scenarios:

- 400 Bad Request: Missing or invalid input data.
- 404 Not Found: When an unknown endpoint is requested.
- 400 Bad Request: Malformatted ID.
- 500 Internal Server Error: For any unhandled errors.
