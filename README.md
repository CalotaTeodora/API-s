# API Endpoints Documentation

This repository contains two different API implementations in Python: one using FastAPI and another using Flask. Both APIs serve as examples of creating RESTful web services.

## FastAPI Implementation (fast_api.py)

FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.6+.

### Endpoints

- **GET /get-item/{item_id}**
  - Description: Retrieve an item by its ID.
  - Parameters:
    - `item_id` (path parameter, integer): The ID of the item to retrieve (between 1 and 9).
  - Response: Returns the item information as JSON.

- **GET /get-by-name/{item_id}**
  - Description: Retrieve an item by its name.
  - Parameters:
    - `name` (query parameter, string, optional): The name of the item.
  - Response: Returns the item information as JSON.

- **POST /create-item/{item_id}**
  - Description: Create a new item with a specific ID.
  - Parameters:
    - `item_id` (path parameter, integer): The ID for the new item.
    - Request Body: JSON object containing `name` (string), `price` (float), and optional `brand` (string) fields.
  - Response: Returns the created item information as JSON.

- **PUT /update-item/{item_id}**
  - Description: Update an existing item by its ID.
  - Parameters:
    - `item_id` (path parameter, integer): The ID of the item to update.
    - Request Body: JSON object containing optional `name` (string), `price` (float), and `brand` (string) fields.
  - Response: Returns the updated item information as JSON.

- **DELETE /delete-item**
  - Description: Delete an item by its ID.
  - Parameters:
    - `item_id` (query parameter, integer): The ID of the item to delete (must be greater than 0).
  - Response: Returns a success message if the item is deleted.

## Flask Implementation (main.py)

Flask is a lightweight WSGI web application framework in Python.

### Endpoints

- **GET /get-user/{user_id}**
  - Description: Retrieve user data by user ID.
  - Parameters:
    - `user_id` (path parameter, string): The ID of the user.
    - `extra` (query parameter, string, optional): Additional information (optional).
  - Response: Returns user information as JSON.

- **POST /create-user**
  - Description: Create a new user.
  - Request Body: JSON object containing `user_id` (string), `name` (string), and `email` (string) fields.
  - Response: Returns the user information as JSON.

### Supported HTTP Methods

The Flask implementation supports the following HTTP methods for API endpoints:
- **GET:** Retrieve data.
- **POST:** Create new data.
- **PUT:** Update existing data.
- **DELETE:** Delete data.

Feel free to explore the code and modify the endpoints to suit your specific use case.

---

**Note:** Ensure you have the necessary dependencies installed to run the respective implementations (FastAPI and Flask). For detailed setup instructions, refer to the documentation of each framework.
