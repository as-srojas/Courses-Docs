# Postman Course: HTTP Methods

## Introduction

HTTP methods define the specific action to be performed on a resource when a request is made to the server. These methods act as verbs, indicating what type of operation is intended. The most commonly used methods are **GET**, **POST**, **PUT**, **PATCH**, and **DELETE**.

In this section, we will explore each HTTP method in detail and understand when and how to use them.

---

## 1. GET Method

### 1.1 Purpose

The **GET** method is used to retrieve data from the server. It requests a representation of the specified resource and **should not modify** the server's state. This method is considered **safe** and **idempotent** (i.e., making multiple identical requests will result in the same response).

### 1.2 Characteristics

- Safe: Does not alter server data.
- Idempotent: Repeating a request returns the same result.
- No Body: The request does not contain a body.
- Cacheable: Responses can be cached for future use.

## 2. POST Method

### 2.1 Purpose

The POST method is used to send data to the server to create a new resource. It often submits form data or JSON payloads. Unlike GET, it is not idempotent, meaning the same POST request made multiple times can result in different outcomes (e.g., creating multiple users).

### 2.2 Characteristics

- Not Safe: It alters server data.
- Not Idempotent: The result changes on repeated requests.
- Has Body: The request body contains the data to be sent.
- Not Cacheable: Typically, responses should not be cached.

## 3. PUT Method

### 3.1 Purpose

The PUT method is used to update an existing resource or create a new one if it does not exist. It sends data to the server to replace the entire resource. PUT requests are idempotent, so sending the same request multiple times will have the same effect.

### 3.2 Characteristics

- Not Safe: Alters server data.
- Idempotent: Repeated requests result in the same outcome.
- Has Body: Contains the data to replace the resource.
- Not Cacheable: Responses are generally not cached.

## 4. PATCH Method

### 4.1 Purpose

The PATCH method is used to apply partial updates to a resource. Unlike PUT, which replaces the entire resource, PATCH modifies only specific fields of a resource. It is also idempotent.

### 4.2 Characteristics

- Not Safe: Alters server data.
- Idempotent: Repeated requests result in the same outcome.
- Has Body: Contains the data to be updated.
- Not Cacheable: Generally not cached.

## 5. DELETE Method

### 5.1 Purpose

The DELETE method is used to remove a resource from the server. It is idempotent, meaning sending the same request multiple times will result in the same outcome.

### 5.2 Characteristics

- Not Safe: Alters server data by removing a resource.
- Idempotent: Repeated requests have the same result.
- No Body: Typically, DELETE requests do not contain a body.
- Not Cacheable: Responses should not be cached.

## 6. Resume

Each HTTP method serves a specific purpose when interacting with APIs. Understanding the correct method to use for each scenario ensures that your requests are efficient, predictable, and aligned with RESTful API practices.

- GET: Retrieve data.
- POST: Create new data.
- PUT: Update or replace data.
- PATCH: Partially update data.
- DELETE: Remove data.