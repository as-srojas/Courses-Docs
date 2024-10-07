# Query Parameters

## 1. What are Query Parameters?

Query parameters are key-value pairs added to the URL to send extra information to the server. They modify the request without affecting the main resource, helping refine how the data is returned or processed.

### 1.1 Syntax

The basic structure of a query parameter is:

?key1=value1&key2=value2

- **`?`**: Marks the start of the query string.
- **`key`**: Name of the parameter.
- **`value`**: Value of the parameter.
- **`&`**: Separates multiple key-value pairs.

### 1.2 Example

To get a list of users with the role of administrator and who are active:

```plaintext
https://api.example.com/users?role=admin&status=active
```

- **role=admin**: Filters users whose role is admin.
- **status=active**: Filters users who are active.

## 2. Types of Query Parameters

### 2.1 Filtering

Allows you to narrow down the dataset returned based on specific conditions.

```plaintext
https://api.example.com/products?category=electronics&brand=sony
```

- **category=electronics**: Filters products belonging to the electronics category.
- **brand=sony**: Filters products from the brand Sony.

### 2.2 Sorting

Enables sorting the results based on an attribute, such as price or creation date.

```plaintext
https://api.example.com/products?sort=price&order=asc
```

- **sort=price**: Sorts the products by price.
- **order=asc**: Sorts in ascending order (lowest to highest).

### 2.3 Pagination

Controls how many results are returned per page and what page to start from.

```plaintext
https://api.example.com/users?page=2&limit=20
```

- **page=2**: Fetches the second page of results.
- **limit=20**: Limits the results to 20 users per page.

### 2.4 Search

Allows searching within a dataset using keywords.

```plaintext
https://api.example.com/search?query=John+Doe
```

- **query=John+Doe**: Searches the system for users matching the name "John Doe".

### 3 Adding Query Parameters in Postman

1. Open **Postman**.
2. Select the **GET** method or any method you are using.
3. Enter the base URL.
4. Click on the **Params** tab below the URL bar.
5. Add key-value pairs for your query parameters.
6. Postman will automatically append the parameters to the URL.

**Example**:

1. Base URL: `https://api.example.com/users`
2. Parameter 1:
   - **Key**: `role`
   - **Value**: `admin`
3. Parameter 2:
   - **Key**: `status`
   - **Value**: `active`

**Postman will generate the complete URL:**

```plaintext
https://api.example.com/users?role=admin&status=active
```

### 4 Avoid Sensitive Data in Query Parameters

Query parameters are part of the URL, meaning they are stored in the browser history and visible in server logs. Avoid sending sensitive information like passwords or authentication tokens in query parameters.

**Example**:

```plaintext
https://api.example.com/users?password=12345
```

### 5 Encode Special Characters

If the parameter values contain special characters (spaces, `&`, `=`), they must be URL-encoded. This ensures that the URL is valid and that the server correctly interprets the parameters.

- Space (` `) → `%20`
- Ampersand (`&`) → `%26`
- Equal sign (`=`) → `%3D`

```plaintext
https://api.example.com/search?query=John%20Doe
```

This searches for the name "John Doe", encoding the space as `%20`.
