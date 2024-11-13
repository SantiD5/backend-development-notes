# What is HTTP?
The Hypertext Transfer Protocol (HTTP) is a protocol used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of the other layers of the network protocol stack.

## What is an HTTP request?
An HTTP request is the way internet communications platforms such as web browsers ask for the information they need to load a website.
each HTTP request contains:
1. HTTP version type
2. a URL
3. an HTTP method(get,post,put,patch,delete)
4. HTTP request headers
5. optional http body

## What is an HTTP method?
An HTTP method indicates the action that the HTTP request expects from the server. Two of the most common HTTP methods are ‘GET’ request expects information back in return (usually in the form of a website) and a ‘POST’ request typically indicates that the client is submitting information to the web server (such as form information, e.g. a submitted username and password).

## What are HTTP request headers?
HTTP headers contain text information stored in key-value pairs, and they are included in every HTTP request (and response, more on that later). These headers communicate core information, such as what browser the client is using and what data is being requested.
![[Pasted image 20241113160237.png]]

## What is in an HTTP request body?
The body of a request is the part that contains the ‘body’ of information the request is transferring. The body of an HTTP request contains any information being submitted to the web server, such as a username and password, or any other data entered into a form.
## What is in an HTTP response?
An HTTP response is what web clients (often browsers) receive from an Internet server in answer to an HTTP request. These responses communicate valuable information based on what was asked for in the HTTP request.
A typical HTTP response contains:
1. an HTTP status code
2. HTTP response headers
3. optional HTTP body
## What’s an HTTP status code?
HTTP status codes are 3-digit codes most often used to indicate whether an HTTP request has been successfully completed. Status codes are broken into the following 5 blocks:
1. 1xx Informational
2. 2xx Success
3. 3xx Redirection
4. 4xx Client Error
5. 5xx Server Error
The “xx” refers to different numbers between 00 and 99.

Status codes starting with the number ‘2’ indicate a success. For example, after a client requests a webpage, the most commonly seen responses have a status code of ‘200 OK’, indicating that the request was properly completed.

If the response starts with a ‘4’ or a ‘5’ that means there was an error and the webpage will not be displayed. A status code that begins with a ‘4’ indicates a client-side error (it is very common to encounter a ‘404 NOT FOUND’ status code when making a typo in a URL). A status code beginning in ‘5’ means something went wrong on the server side. 
## What are HTTP response headers?
Much like an HTTP request, an HTTP response comes with headers that convey important information such as the language and format of the data being sent in the response body.

Example of HTTP response headers from Google Chrome's network tab:

![[Pasted image 20241113160559.png]]
## What is in an HTTP response body?

Successful HTTP responses to ‘GET’ requests generally have a body which contains the requested information. In most web requests, this is HTML data that a web browser will translate into a webpage.
