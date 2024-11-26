---
layout: default
title: API Requests
nav_order: 5
has_children: false
permalink: docs/api-requests
---

# API Request Capabilities


### Overview  
This API Test Automation Framework is designed to provide a simple and efficient way to automate testing of RESTful APIs. It provides a fluent and intuitive API for setting up requests, sending them, and validating responses.  

### Key Features  
- **Ease of Use**: Simple methods to configure and send API requests.  
- **Flexibility**: Supports multiple media types and HTTP request methods.  
- **Scalability**: Designed to be extendable for various test scenarios.  
- **Reusability**: Encapsulation of request-building logic for cleaner test code.  

---

### Usage Guide  

#### Class Overview  
- **`Request`**: The main class for configuring and sending API requests.  

---

#### Methods  

```java
Request.set(String url) 
```

Sets the base URL for the API request.  
- **Parameter**: `url` - The API endpoint (e.g., `https://api.example.com/resource`).  

```java
Request.setMediaType(String mediaType)
```

Specifies the media type of the request.  
- **Parameter**: `mediaType` - The type of the media, such as `application/json` or `application/xml`.  

```java
 Request.setHeader(String key, String value)
 ```
Adds a header to the request.  
- **Parameters**:  
  - `key` - The header name (e.g., `Authorization`).  
  - `value` - The header value (e.g., `Bearer token`).  

```java
Request.setQueryParams(String key, String value)
```

Adds query parameters to the request URL.  
- **Parameters**:  
  - `key` - The query parameter name.  
  - `value` - The query parameter value.  

```java
Request.setPayload(String payload)
```

Sets the request body.  
- **Parameter**: `payload` - The payload content in string format (e.g., JSON or XML).  

```java
Request.send(String reqType)
```

Sends the API request using the specified HTTP method.  
- **Parameter**: `reqType` - The HTTP method (e.g., `GET`, `POST`, `PUT`, `DELETE`).  

```java
Request.response()
```

Retrieves the response object. This object contains the raw response returned by the API.  

```java
Request.getResponseString()
```

Returns the response content as a string.  

```java
Request.reset()
```

Resets the request object by closing all connections and clearing previous configurations.  

---

### Example Usage  

```java
// Setting up a GET request
Request.set("https://api.example.com/resource");
Request.setMediaType("application/json");
Request.setHeader("Authorization", "Bearer sample_token");
Request.setQueryParams("key1", "value1");
Request.setQueryParams("key2", "value2");

// Sending the request
Request.send(ReqType.GET);

// Retrieving and printing the response
String response = Request.getResponseString();
System.out.println("Response: " + response);

// Reset the request object
Request.reset();
```

---

### Advanced Usage  

#### Example: POST Request with JSON Payload  

```java
// Setting up a POST request
Request.set("https://api.example.com/resource");
Request.setMediaType("application/json");
Request.setHeader("Authorization", "Bearer sample_token");
Request.setPayload("{\"key\":\"value\"}");

// Sending the request
Request.send(ReqType.POST);

// Handling the response
if (Request.getStatusCode() == 200) {
    System.out.println("Success: " + Request.getResponseString());
} else {
    System.err.println("Error: " + Request.getStatusCode());
}

// Resetting the request object
Request.reset();
```

---

### Error Handling  

#### Common Errors and Solutions  

1. **Invalid URL**  
   Ensure the URL passed to `Request.set()` is valid and includes the protocol (e.g., `https`).  

2. **Unsupported Media Type**  
   Check the media type passed to `Request.setMediaType()`. Supported types include `application/json`, `application/xml`, etc.  

3. **Missing Headers**  
   Certain APIs require specific headers (e.g., `Authorization`). Use `Request.setHeader()` to include them.  

---

### Best Practices  

1. **Reuse Headers**  
   If certain headers are common across multiple requests, encapsulate them in utility methods or configuration files.  

2. **Payload Management**  
   Use external JSON/XML files for complex payloads to maintain readability.  

3. **Assertion Integration**  
   Combine the framework with assertion libraries like TestNG or JUnit for automated validation of responses.  

4. **Connection Reset**  
   Always call `Request.reset()` after tests to avoid memory leaks or stale connections.  

---

### Extending the Framework  

#### Adding Custom Methods  
To add custom functionality, extend the `Request` class or use utility classes to augment existing methods.  

---

### FAQs  

**Q: Can I use this framework with CI/CD pipelines?**  
Yes, integrate it with tools like Jenkins, GitHub Actions, or Azure Pipelines for continuous testing.  

**Q: Does it support asynchronous requests?**  
Currently, the framework is designed for synchronous requests. Asynchronous support can be added as an extension.  





