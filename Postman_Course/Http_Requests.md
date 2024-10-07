# Postman Course: HTTP, Requests, and Methods

## Introduction

In this module, you will learn the fundamentals of **HTTP**, explore different types of **HTTP requests**, and understand how **HTTP methods** are used in APIs. By the end, you'll be able to interact with APIs using Postman confidently.

## 1. What is HTTP?

**HTTP (HyperText Transfer Protocol)** is the foundation of data communication on the web. It is a protocol used for transferring hypertext requests and information between a web browser (client) and a server.

### 1.1 How HTTP Works

- **Client**: The device making the request (e.g., a browser or Postman).
- **Server**: The system that processes the request and sends back a response.
- **HTTP Request**: The message sent by the client to the server, containing the requested resource or data.
- **HTTP Response**: The message returned by the server, containing the requested resource or a status message.

## 2. What is an HTTP Request?

An **HTTP request** is a structured message sent from the client to the server. It typically contains:

- **Method**: The type of operation to be performed (e.g., GET, POST).
- **URL**: The address of the resource (API endpoint).
- **Headers**: Metadata about the request (e.g., content type, authorization).
- **Body**: Data sent to the server (optional, depending on the method).

### 2.1 Components of an HTTP Request

- **Request URL**: The endpoint where the request is sent.
- **Method**: Defines the type of action (GET, POST, PUT, DELETE, etc.).
- **Headers**: Provide additional information like content type and authorization.
- **Body**: Contains the data being sent, applicable in methods like POST and PUT.

Example of a basic HTTP request:

```plaintext
GET /users HTTP/1.1
Host: api.example.com
Content-Type: application/json
Authorization: Bearer token123
```

## 3. Headers

### 3.2 Adding Headers

Click the Headers tab in the request section.

Add key-value pairs for the required headers (e.g., Authorization, Content-Type).

Example:

```plaintext
Authorization: Bearer token123
Content-Type: application/json
```

## 4. Status Codes

After making an HTTP request, the server responds with a status code indicating the result of the request.

- **200** OK: The request was successful.
- **201** Created: A new resource has been created (used with POST).
- **400** Bad Request: The server could not understand the request.
- **401** Unauthorized: Authentication is required or failed.
- **404** Not Found: The requested resource could not be found.
- **500** Internal Server Error: The server encountered an unexpected condition.
