# Reading for Day 8:

- [API Design Best Practices](<https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design>)

1. What does REST stand for?
  REST: REpresentational State Transfer
2. REST APIs are designed around a _____.
  Resources
3. What is an identifier of a resource. Give an example.
  A resource identifier is a URI (Uniform Resource Identifier). EX:
  `https://adventure-works.com/orders/1`
4. What are the most common HTTP verbs?

    - GET
    - POST
    - PUT
    - PATCH 
    - DELETE

5. What should the URIs be based on?
  URIs should be based on the resource.
6. Give an example of a good URI.
  `https://adventure-works.com/orders`
7. What does it mean to have a 'chatty' web API? Is this a good or a bad thing?
  A "chatty" API is a bad thing because it can slow down the system due to numerous I/O operations.
8. What status code does a successful `GET` request return?
  Typically, it gets an HTTP status code of 200
9. What status code does an unsuccessful `GET` request return?
  In the event that the resource cannot be found, an HTTP status code of 404 would be returned.
10. What status code does a successful `POST` request return?
  A successfully created POST returns an HTTP status code of 201
11. What status code does a successful `DELETE` request return?
  When a DELETE operation is successful, it should return a status code of 204

## Bookmark / Skim

- [REGEXr](<https://regexr.com/>)

1. How would you write your name using REGEX?

- [REGEX Tutorial](<https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285>)
- [REGEX 101](<https://regex101.com/>)
