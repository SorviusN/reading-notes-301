# Reading Notes 8

### What does REST stand for?
Representational State Transfer.
### REST APIs are designed around a ____.
resource, any kind of object, data or service that can be accessed by the client.
### What is an identifer of a resource? Give an example.
An identifier for a resource could be URI that uniquely identifies that resource. such as:

``` js
'https://adventure-works.com/orders/1'0
```

### What are the most common HTTP verbs?
 The most common operations are GET, POST, PUT, PATCH, and DELETE.

### What should the URIs be based on?
Nouns.
### Give an example of a good URI.
https://adventure-works.com/orders - has a noun at the end vs. a verb like "create-order".
### What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
Chatty APIs are not ideal. They are APIs that expose a large number of small resources. They require a client to send multiple reqs to find all data that it needs.
### What status code does a successful GET request return?
A successful GET method typically returns HTTP status code 200 (OK).
### What status code does an unsuccessful GET request return?
 If the resource cannot be found, the method should return 404 (Not Found).
### What status code does a successful POST request return?
If a POST method creates a new resource, it returns HTTP status code 201 (Created).
### What status code does a successful DELETE request return?
If the delete operation is successful, the web server should respond with HTTP status code 204.
