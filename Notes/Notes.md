# Welcome To Journey Of BackEnd Engineering



# Hypertext Transfer Protocol (HTTP):

<br>
<img src="./assets/imgs/http.png" width="100%" height="230px"> 
</br>

HTTP stands for Hypertext Transfer Protocol, and it is the foundation of data communication on the World Wide Web (WWW). It is an application layer protocol used for transmitting and receiving data on the internet (Request - Response). HTTP is the protocol that enables web browsers to request and display web pages and allows users to navigate and interact with websites.


<br>
    <img src="./assets/imgs/localhost-http.png"> Local Host using http://
</br>
</br>

## Some key points :

- **Client-Server Model :**
HTTP operates in a client-server model. The client (usually a web browser) sends requests to a server (a web server) for specific resources, such as web pages, images, or other data. The server then processes the request and sends a response back to the client.


- **Stateless Protocol :**
HTTP is considered a stateless protocol, which means each request-response cycle is independent of previous ones. In other words, the server doesn't inherently retain information about previous requests from the same client. To maintain state between requests, web applications often use techniques like cookies or sessions.

- **Text-Based :**
HTTP messages are typically text-based, making them human-readable. An HTTP request consists of a request line, headers, and an optional message body. The response includes a status line, headers, and a response body (such as an HTML page).

- **Connection-Oriented :**
HTTP can be either connection-oriented or connectionless. HTTP/1.0 used a connectionless model, where a new connection was established for each request-response cycle. HTTP/1.1 introduced a connection-oriented model with features like persistent connections, which allow multiple requests and responses to be sent over a single connection, reducing latency.

- **State Management :**
HTTP itself doesn't provide built-in mechanisms for managing session state or authentication. Web developers often rely on cookies and HTTP headers (e.g., Authorization header) to handle these aspects.

- **Secure Version :**
HTTPS (HTTP Secure) is a secure version of HTTP that uses encryption to protect data transmission between the client and the server. It is widely used for secure communication on the web, especially when sensitive information like login credentials or payment details are involved.

- **Methods :**
HTTP defines various request methods, such as GET (retrieve data), POST (send data to be processed), PUT (update data), DELETE (remove data), and others. These methods determine the action to be performed on the resource identified in the URL.


## HTTP Anatomy :
HTTP (Hypertext Transfer Protocol) messages, both requests and responses, have a specific structure or "anatomy." They consist of several components, including headers and an optional message body.














## The Journey of an HTTP Request to the Backend




# Request - Response



# Object - Mapper (Jackson)
