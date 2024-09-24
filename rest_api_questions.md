
### REST API Questions

1. **What is a RESTful API?**
   - **Answer:** A RESTful API (Representational State Transfer) is an architectural style that uses HTTP requests to access and manipulate data. It is stateless and designed to operate over the web, allowing interaction with resources identified by URLs.

2. **What are the main principles of REST?**
   - **Answer:**
     - **Statelessness:** Each request from the client to the server must contain all the information needed to understand and process the request.
     - **Client-Server Architecture:** The client and server are separate entities, allowing for independent development.
     - **Cacheability:** Responses must define themselves as cacheable or non-cacheable to improve performance.
     - **Layered System:** A client cannot tell whether it is connected directly to the server or through an intermediary.
     - **Uniform Interface:** A standardized way of interacting with resources through defined endpoints.

3. **What are HTTP methods commonly used in REST APIs?**
   - **Answer:**
     - **GET:** Retrieve data from the server.
     - **POST:** Create a new resource on the server.
     - **PUT:** Update an existing resource or create a new resource if it doesn't exist.
     - **PATCH:** Apply partial modifications to a resource.
     - **DELETE:** Remove a resource from the server.

4. **What is the difference between PUT and PATCH?**
   - **Answer:** 
     - **PUT** is used to update an entire resource or create it if it doesn't exist. It requires sending the full representation of the resource.
     - **PATCH** is used for partial updates, allowing only the fields that need to be changed to be sent.

5. **How do you handle versioning in REST APIs?**
   - **Answer:** Versioning can be handled through:
     - **URI Versioning:** Including the version number in the URL (e.g., `/api/v1/resource`).
     - **Query Parameters:** Adding a version parameter (e.g., `/api/resource?version=1`).
     - **Header Versioning:** Using custom headers to specify the API version.

6. **What are status codes in REST APIs, and can you give some examples?**
   - **Answer:** Status codes indicate the outcome of an API request. Examples include:
     - **200 OK:** The request succeeded.
     - **201 Created:** A resource was successfully created.
     - **204 No Content:** The request succeeded, but there's no content to return.
     - **400 Bad Request:** The request was malformed.
     - **401 Unauthorized:** Authentication is required and has failed or not been provided.
     - **404 Not Found:** The requested resource could not be found.
     - **500 Internal Server Error:** An unexpected error occurred on the server.

7. **What is the difference between REST and SOAP?**
   - **Answer:**
     - **REST**: Uses standard HTTP methods, is stateless, and can return various data formats (JSON, XML). It is generally easier to work with and more lightweight.
     - **SOAP**: A protocol that relies on XML, includes built-in error handling, and supports WS-* standards for security and transactions. It is heavier and more complex.

8. **How can you secure a REST API?**
   - **Answer:** Security can be implemented using:
     - **Authentication:** OAuth, JWT (JSON Web Tokens), API keys.
     - **Authorization:** Role-based access control (RBAC).
     - **HTTPS:** Encrypting data in transit using TLS/SSL.
     - **Input Validation:** Ensuring that user inputs are validated and sanitized.
     - **Rate Limiting:** Protecting against abuse by limiting the number of requests.

9. **What is HATEOAS in REST?**
   - **Answer:** HATEOAS (Hypermedia as the Engine of Application State) is a constraint of REST that allows clients to interact with the application entirely through hypermedia links provided dynamically by the server in the API responses, enabling discoverability.

10. **What are some common tools for testing REST APIs?**
    - **Answer:** Common tools include:
      - **Postman:** A user-friendly tool for sending requests and viewing responses.
      - **cURL:** A command-line tool for making HTTP requests.
      - **Swagger (OpenAPI):** For documenting and testing APIs.
      - **Insomnia:** A powerful REST client for debugging APIs.
