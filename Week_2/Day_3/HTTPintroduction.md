## HTTP Flow

HTTP is a request-response based protocol. A client makes a request to an HTTP server, immediately also sending a message asking for a specific resource, which the server sends down as a response. 

## HTTP Requests
when a client wants to communicate with a server it issues a request. An HTTP request is made up of many components, two of those are

1. PATH
2. Method

The path says what resource the client wants to act on, and the method says what action it would like to perform.

## HTTP Methods
GET: used to "get" some data from the server

POST: usually used to create some new data

PUT: generally used for editing existing data on the server

DELETE: used to delete some existing data

## Paths and URL
Uniform Resource Locator, or URL

The path is a part of the URL.

- Protocol
- Domain (or Host)
- Port
- Resource Path
- Query Parameters
- Anchor

## HTTP Responses
When server receives a request from client, it reads path and method. If request is GET /dogs, it will fetch all the data about dogs and responds back. 

Response has these components: (and many more)
1. Status Code

When e.g. page not found or an error, server uses status code to send this error info. 
Some important status codes are below:
* 200: "Everything went great!"
- 201: "The request has succeeded and a new resource has been created as a result."
- 404: "Resource was not found."
- 500: "The server had an error."

2.  Body

Body contains the actual data client requested from the server. 

Conclusion:
- HTTP is a request-response protocol, where the client makes requests and the server sends responses
- HTTP is a text based protocol, making it easy to read and understand for humans
- HTTP requests must contain the verb/method (eg: GET) and the Path (eg: /about)
- HTTP requests aren't always to receive data, but sometimes to save data, like when we submit a form on a website. This is done via a POST instead of a GET
- Requests and responses both contain key-value based headers (eg: Accept-Language: fr, Content-Type: text/html, etc.)