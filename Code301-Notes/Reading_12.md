# Reading for Day 12:

- [Status Codes Based On REST Methods](<https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/>)

1. In your own words, describe what each group of status code represents:
    - 100's = these provide information letting the client know that the request has been received
    - 200's = these are `SUCCESS!` codesletting the client know that the request met all the validation requirements
    - 300's = these are for redirection... the resource isn't available at that location anymore
    - 400's = these are `client error` codes... the request to the server was not validated - check that the input requirements are correct
    - 500's = these are `server error` codes... this could be an overwhelmed server or unreachable server
  
2. What is a status code 202?
    - ***ACCEPTED*** - Used in asynchronous processing... and means that the input was valid and the resouce will be available

3. What is a status code 308?
    - ***PERMANENT REDIRECT*** - You need to use another url

4. What code would you use if an update didn't return data to the client?
    - A code ***204 - NO CONTENT***

5. What code would you use if a resource used to exist but no longer does?
    - A status code ***410***

6. What is the `Forbidden` status code?
    - A status code ***403***

## Additional Resources

### Videos

- [Build A REST API With Node.js, Express, & MongoDB -Quick](<https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw>)

1. What do we need to pull our MongoDB database string out of our server and put it into our `.env`?
    - `npm i --save-dev dotenv`

2. What is middleware?
    - Code that runs between the server and the client

3. What does `app.use(express.json())` do?
    - Let's the server accept json used in the body of a request

4. What does the `/:id` mean in a route?
    - Parameter accessed by using `req.params.id`

5. What is the difference between `PUT` and `PATCH`?
    - 

6. How do you make a default value in a schema?
    - 

7. What does a `500` error status code mean?
    - Server Error

8. What is the difference between a status `200` and a status `201`?
    - 
