# BackEnd

## What is application programming interface (API)?

The API provides the ability to provide access to a set of commonly used functions. And from there it is possible to exchange data between applications.

API Websocket : JSON
API Rest: GET, PUT, POST, UPDATE, DELETE

## What are web services?

Webservice là tập hợp các giao thức và tiêu chuẩn mở được sử dụng để trao đổi dữ liệu giữa các ứng dụng hoặc giữa các hệ thống.

## What is the difference web services and API services?

The key distinction is that web services are a type of API: All web services are APIs, but not all APIs are web services. 'API' is the broader category because, by definition, it refers to any software component that acts as an intermediary between two otherwise disconnected applications.

Web services: two computers in a network
API: two applications

## What is representational state transfer (REST)?

- Is an architectural style used in the communication between the client and the web server.
- Use HTTP
- Advantages: REST-like interactions take place on structures that are familiar to anyone who is used to using the HTTP Protocol.
- Disadvantages: The limitations of HTTP also become limitations of the REST architecture.
  _For example, HTTP does not store state information between cycles when responding to requests, and as such REST-based applications fall into stateless state and any state management tasks must be performed by the server. performed by the customer._

## What is Restful API)? How does it work?

RESTful API is a standard used in the design of APIs for web applications to manage resources. RESTful is one of the popular API design styles used today to let different applications (web, mobile...) communicate with each other.

GET, POST, PUT/PATCH, DELETE,...

- How does it work?
  REST works mainly on the HTTP protocol. The above basic operations will use their own HTTP methods.

These methods or operations are often called CRUD corresponding to Create, Read, Update, Delete - Create, Read, Edit, Delete.

## What is the difference REST API and SOAP?

| REST API                                                                  | SOAP                                           |
| ------------------------------------------------------------------------- | ---------------------------------------------- |
| Relies on REST (Representational State Transfer) architecture using HTTP. | Relies on SOAP (Simple Object Access Protocol) |
| XML, JSON - Stateless                                                     | Transports data in standard XML format.        |
| GET, POST, PUT, DELETE                                                    | WSDL                                           |
| HTTP, HTTPS                                                               | HTTP, HTTPS, SMTP, XMPP                        |
| Less structured -> less bulky data                                        | Highly structured/typed                        |

## What is the difference REST API and GrapqQL API?

| REST API                                                                | GraphAPI                                                             |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Follows server-driven architecture                                      | Follows client-driven architecture                                   |
| arranged in terms of endpoints                                          | organized in terms of a schema                                       |
| The endpoint you call in REST is the identity of an object              | The identity is separated from how you fetch it                      |
| The shape and size of the resource are determined by the server in REST | server determines available resources                                |
| hard to get consistency across all platforms                            | high consistency across all platforms                                |
| It is difficult to get consistency across all operating systems         | Provides consistent and high-quality UX across all operating systems |
| It offers flexible public API that can easily enable new applications.  | Partners of GraphQL require API customization                        |

## What is Hypertext Transfer Protocol (HTTP)?

Is the set of rules for transferring files -- such as text, images, sound, video and other multimedia files -- over the web.

HTTP is an application protocol that runs on top of the TCP/IP suite of protocols.

## What is the difference HTTP and HTTPS?

| HTTP                        | HTTPS                  |
| --------------------------- | ---------------------- |
| port 80                     | port 443               |
| Application Layer           | Transport Layer        |
| NO Encryption               | Encryption             |
| NO Certificates             | SSL Certificates       |
| DONT improve search ranking | improve search ranking |
| faster                      | slower                 |
