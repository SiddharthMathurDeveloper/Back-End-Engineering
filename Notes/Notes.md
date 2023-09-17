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

### What is a Header ?? :
In the context of computer science and networking, a "header" refers to a block of information that precedes or follows a data block and provides metadata or control information about the data it accompanies. Headers are commonly used in various protocols and file formats to convey important details about the associated data. Here are a few common uses of headers:




- **HTTP Headers :**

In the **Hypertext Transfer Protocol (HTTP)**, headers are used to transmit metadata about an HTTP request or response. They provide information such as the content type, content length, caching directives, authentication details, and more. HTTP headers are crucial for the proper functioning of web communication between clients (e.g., web browsers) and servers (e.g., web servers).

- **Email Headers :**

In email communication, **email headers** contain information about the sender, recipient, subject, date, and routing details of an email message. These headers help email clients and servers process and display emails correctly.

- **Network Headers :**

In networking, data packets typically include a header that contains information like source and destination addresses, routing information, and protocol-specific data. For example, in the **IP (Internet Protocol)** header, you'll find IP addresses, time-to-live (TTL), and more.

- **File Format Headers :**

Many file formats, such as image files (e.g., JPEG), audio files (e.g., MP3), and document files (e.g., PDF), have headers that store metadata about the file, including details about its content, dimensions, encoding, and more.

- **Compression Headers :**

In compressed files, headers provide information needed for decompression, such as the compression algorithm used and additional parameters.

- **Protocol Headers :**

Various network protocols, such as TCP, UDP, and DNS, use headers to convey control information relevant to the specific protocol. For example, TCP headers include details about sequence numbers, acknowledgment numbers, and flags.


**Note: Headers are essential for the proper interpretation and processing of data in different contexts. They help systems understand how to handle, route, and display data, making communication and data exchange more reliable and efficient. The format and content of headers vary depending on the specific protocol or file format in use.**


### Does Request and Response header same or different ?? :
Request headers and response headers in HTTP messages are different. They serve distinct purposes and contain information relevant to the particular side of the communication


### But some headers are same irrespective type (Request,Response) header is different ?? :
Some headers that can appear in both request and response messages, but they may serve slightly different purposes or convey related information in the context of the client's request and the server's response

### Types Of Http Headers ?? :
 - Request Header
 - Response Header











## The Journey of an HTTP Request to the Backend




# Request - Response



# Object - Mapper (Jackson)
