# The Internet

What is the Internet?
Ans: 

# Basic Terminologies

1. Client-side: The part of the web application that runs on user's browser (client)
2. Server-side: The part of the web application that runs on a server

The above are in terms of web development. A server-database interaction can also be seen as client-server but that's not running on a user's device.

3. Frontend: Part of the application that user sees and interacts with
4. Backend: Part of the application that processes data, handles logic and operations 

Note: Client and frontend are not the same. Client deals with the device of the user, frontend deals with the UI/UX of the application

5. HTTP - HyperText Transfer Protocol: 
- TCP/IP based application layer communication protocol that standardizes how client and server communicate.
- Follows client-server model
- Defines how content is requested and transmitted across the Internet
- HTTP/0.9 was ONLY a GET method (GET /index.html)
- HTTP/1.0 added more to the protocol such as POST, req/res formats changed, headers got added to res and req, status codes, caching, etc
- HTTP/1.1 was the first standardized protocol
- Stateless protocol, i.e, server does not keep any data about between two requests

Fun fact: HTTP was developed at CERN along with HTML and WWW (World Wide Web)
- WWW: Interconnected system of hypertext documents

## HTTP Requests
- There are different request methods - GET, POST, PUT, DELETE
- GET, i.e, get a resource from the server
- POST, i.e, post a resource to the server

GET req ex:

    GET / HTTP/1.1 
    Host: developer.mozilla.org
    Accept-Language: fr

POST req ex:

    POST /contact_form.php HTTP/1.1
    Host: developer.mozilla.org
    Content-Length: 64
    Content-Type: application/x-www-form-urlencoded
    name=Joe%20User&request=Send%20me%20one%20of%20your%20catalogue

## HTTP Response
Server response ex:

    HTTP/1.1 200 OK
    Content-Type: text/html; charset=utf-8
    Content-Length: 55743
    Connection: keep-alive
    Cache-Control: s-maxage=300, public, max-age=0
    Content-Language: en-US
    Date: Thu, 06 Dec 2018 17:37:18 GMT
    ETag: "2e77ad1dc6ab0b53a2996dfd4653c1c3"
    Server: meinheld/0.6.1
    Strict-Transport-Security: max-age=63072000
    X-Content-Type-Options: nosniff
    X-Frame-Options: DENY
    X-XSS-Protection: 1; mode=block
    Vary: Accept-Encoding,Cookie
    Age: 7

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>A simple webpage</title>
</head>
<body>
  <h1>Simple HTML webpage</h1>
  <p>Hello, world!</p>
</body>
</html>
```

- Structure is:
    1. Status line 
    2. Information about data sent back to client
    3. Data block

### Status codes
- Codes that indicate how a HTTP request was handled
    1. 200-299: Successful responses
    2. 300-399: Redirect messages
    3. 400-499: Client error responses
    4. 500-599: Server error responses

# HTTPS
- HTTPS stands for HTTP Secure
- HTTPS encrypts data whereas HTTP does not

# Databases
- A database is an organized collection of structured information, or data, typically stored electronically in a computer system. 
- Basically, a place to store data
- Two main types of database: SQL and NoSQL
- Why have different types in first place? To have the option of how you want to structure your data that you want to store.

## SQL
- SQL database is like a large Excel sheet, there's tables with rows and columns
- Structured Query Language
- You get or update data using this query language called SQL
- aka relational databases
- Some popular SQL DBs: Oracle MySQL, PostgreSQL

## NoSQL
- Stands for Not Only SQL
- aka non-relational databases
- Categories of NoSQL DBs:
    a. Document store
    b. Graph databases
    c. Key-value stores 
    d. Wide-column stores
- Popular NoSQL DBs: MongoDB, Supabase
