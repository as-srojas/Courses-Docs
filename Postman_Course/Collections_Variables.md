# Postman Course: Collections & Variables

## Introduction

In this module, you will learn how to use **Postman Collections** and **Variables** to organize your API requests efficiently and manage dynamic data across requests. 

---

## 1. What is a Postman Collection?

A **Postman Collection** is a group of saved API requests organized into folders. Collections help to:
- Group related requests.
- Save time by reusing requests.
- Organize and document API workflows.
  
### 1.1 Why Use Collections?

- **Organization**: Keep API requests grouped logically.
- **Sharing**: Easily share your APIs with teammates.
- **Automation**: Use with Postman Runner or Newman to automate testing.

### 1.2 How to Create a Collection

1. Open **Postman**.
2. Click the **Collections** tab on the left sidebar.
3. Click the **New Collection** button.
4. Give your collection a name and description (optional).
5. Add requests to your collection by clicking the **Add Request** button.

---

## 2. Variables in Postman

**Variables** in Postman allow you to store and reuse values within your collections. They can make your requests more dynamic and maintainable by avoiding hardcoding values.

### 2.1 Types of Variables

1. **Global Variables**: Accessible from any request in your workspace.
2. **Collection Variables**: Scoped to the collection where they are defined.
3. **Environment Variables**: Scoped to the selected environment (e.g., staging, production).
4. **Local Variables**: Temporary variables used only in a single request.

### 2.2 Defining Variables

You can define variables directly within Postman:
- Navigate to the **Collections** tab.
- Click on the **Variables** tab of the collection.
- Add a **Variable Name** and **Initial Value** (default) and optionally set a **Current Value**.

Alternatively, variables can be set programmatically using the `pm` object in **Pre-request Scripts** or **Tests** sections:
```
pm.collectionVariables.set("variable_key", "value");
pm.environment.set("env_variable_key", "value");
```

### 2.3 Using Variables in Requests

- Use the {{variable_name}} syntax in the request URL, headers, or body.
For example:

```
https://api.example.com/{{userId}}/posts
```