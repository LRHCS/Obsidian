The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load web pages using hypertext links.
## What’s in an HTTP request?
An HTTP request is the way internet communications platforms such as web browsers ask for the information they need to load a website.
1.  HTTP version type
2.  a URL
3.  an HTTP method
4.  HTTP request headers
5.  Optional HTTP body.
#### What’s an HTTP method?
An HTTP method, sometimes referred to as an HTTP verb, indicates the action that the HTTP request expects from the queried server. For example, two of the most common HTTP methods are ‘GET’ and ‘POST’; a ‘GET’ request expects information back in return (usually in the form of a website), while a ‘POST’ request typically indicates that the client is submitting information to the web server (such as form information, e.g. a submitted username and password).

#### What are HTTP request headers?
HTTP headers contain text information stored in key-value pairs, and they are included in every HTTP request

#### What’s in an HTTP request body?
The body of a request is the part that contains the ‘body’ of information the request is transferring. The body of an HTTP request contains any information being submitted to the web server, such as a username and password, or any other data entered into a form.
## What’s in an HTTP response?

An HTTP response is what web clients (often browsers) receive from an Internet server in answer to an HTTP request. These responses communicate valuable information based on what was asked for in the HTTP request.

A typical HTTP response contains:

1.  an HTTP status code
2.  HTTP response headers
3.  optional HTTP body

#### What’s an HTTP status code?

HTTP status codes are 3-digit codes most often used to indicate whether an HTTP request has been successfully completed. Status codes are broken into the following 5 blocks:

1.  1xx Informational
2.  2xx Success
3.  3xx Redirection
4.  4xx Client Error
5.  5xx Server Error

#### What are HTTP response headers?

Much like an HTTP request, an HTTP response comes with headers that convey important information such as the language and format of the data being sent in the response body.

Example of HTTP response headers from Google Chrome's network tab:
#### What’s in an HTTP response body?

Successful HTTP responses to ‘GET’ requests generally have a body which contains the requested information. In most web requests, this is HTML data which a web browser will translate into a web page.

---
HTTP methods are a way for the client to show their intended action when making an HTTP request. There are a lot of HTTP methods but we'll cover the most common ones, although mostly you'll deal with the GET and POST method.

**GET Request**

This is used for getting information from a web server.  

**POST Request**

This is used for submitting data to the web server and potentially creating new records  

**PUT Request**

This is used for submitting data to a web server to update information

**DELETE Request**  

This is used for deleting information/records from a web server.

**HTTP Status Codes:**

In the previous task, you learnt that when a HTTP server responds, the first line always contains a status code informing the client of the outcome of their request and also potentially how to handle it. These status codes can be broken down into 5 different ranges:

**100-199 - Information Response**

These are sent to tell the client the first part of their request has been accepted and they should continue sending the rest of their request. These codes are no longer very common.

**200-299 - Success**

This range of status codes is used to tell the client their request was successful.

**300-399 - Redirection**

These are used to redirect the client's request to another resource. This can be either to a different webpage or a different website altogether.

**400-499 - Client Errors**

Used to inform the client that there was an error with their request.

**500-599 - Server Errors**

This is reserved for errors happening on the server-side and usually indicate quite a major problem with the server handling the request.

**Common HTTP Status Codes:**  

There are a lot of different HTTP status codes and that's not including the fact that applications can even define their own, we'll go over the most common HTTP responses you are likely to come across:

**200 - OK**

The request was completed successfully.

**201 - Created**

A resource has been created (for example a new user or new blog post).

**301 - Permanent Redirect**

This redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead.

**302 - Temporary Redirect**

Similar to the above permanent redirect, but as the name suggests, this is only a temporary change and it may change again in the near future.

**400 - Bad Request**

This tells the browser that something was either wrong or missing in their request. This could sometimes be used if the web server resource that is being requested expected a certain parameter that the client didn't send.

**401 - Not Authorised**

You are not currently allowed to view this resource until you have authorised with the web application, most commonly with a username and password.

**403 - Forbidden**

You do not have permission to view this resource whether you are logged in or not.

**405 - Method Not Allowed**

The resource does not allow this method request, for example, you send a GET request to the resource /create-account when it was expecting a POST request instead.

**404 - Page Not Found**

The page/resource you requested does not exist.

**500 - Internal Service Error**

The server has encountered some kind of error with your request that it doesn't know how to handle properly.

**503 - Service Unavailable**

This server cannot handle your request as it's either overloaded or down for maintenance.