### What is ASP.NET Web API (Application programming interface)?
- it is a framework that allows you to create web services that can be consumed by other applications or devices. that is http based services on top of the .Net Framework.
- These services can then be consumed by a broad range of clients like browsers, mobile devices, and desktop applications.
### What is Rest (Representational State Transfer)?
- it is an architectural pattern used for exchange data.
- data is exchange between client and server between the distributed environment. Distributed environment means client can be on any platform and server can be on any platform.
- The Rest architectural pattern treats each service as a resource and the client can access that resource through standard HTTP methods like GET, POST, PUT, DELETE, etc.
### What are the restful services?
- The REST architectural pattern specifies a set of constraints that a system should be adhered to. Here are the REST constraints.
    1. Client-server architecture
       - This constraint specifies that a Client sends a request to the server and the server sends a response back to the client.
       - This separation of concerns supports the independent development of both client-side and server-side logic. 
       - That means client applications and server applications should be developed separately without any dependency on each other. A client should only know resource URIs and that’s all. 
       - Severs and clients may also be replaced and developed independently as long as the interface between them is not altered.
    2. Stateless Constraint
       - The stateless constraint specifies that the communication between the client and the server must be stateless between requests. 
       - That means the server should not be storing anything on the server related to the client.
       - The request from the client should contain all the necessary information so that the server can identify the client and can process that request. This ensures that each request can be treated independently by the server.
    3. Uniform interface  
       - The Uniform interface constraint specifies that the client should be able to consume resources using standard HTTP methods like GET, POST, PUT, and DELETE.
       - The HTTP verb (GET, PUT, POST, PATCH, and DELETE) that is sent with each request tells the API what to do with the resource.
       - Each resource is identified by a specific URI (Uniform Resource Identifier).  
    4. Cacheable
       - In real-time applications, some data provided by the server is not changed that frequently like the list of Countries, the list of States,  the list of cities, and some master data. 
       - The Cacheable Constraint says that let the client know how long this data is good for so that the client does not have to come back to the server for that data over and over again.
    5. Layered system
       - REST allows us to use a layered system architecture where we deploy the APIs in server A, and store data on server B and authenticate requests in server C. 
       - For example, a client cannot ordinarily tell whether it is connected directly to the server or to an intermediary along the way.
### Different between REST and SOAP?
- SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.
- The SOAP is an XML-based protocol whereas REST is not a protocol rather it is an architectural pattern i.e. resource-based architecture.                         
- SOAP has specifications for both stateless and state-full implementation whereas REST is completely stateless.
- SOAP enforces message format as XML whereas REST does not enforce message format as XML or JSON.
- The SOAP message consists of an envelope that includes SOAP headers and body to store the actual information we want to send whereas REST uses the HTTP build-in headers (with a variety of media-types) to store the information and uses the HTTP Methods such as GET, POST, PUT, PATCH, and DELETE  to perform CRUD operations.
- SOAP uses interfaces and named operations (i.e. Service Contract and Operation Contract) to expose the service whereas to expose resources (service) REST uses URI and methods like (GET, PUT, POST, PATCH, and DELETE).
- SOAP Performance is slow as compared to REST.