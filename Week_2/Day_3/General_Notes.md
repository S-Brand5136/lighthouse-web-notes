### General Notes

- HTTP (`Hyper Text Transfer Protocol`) is a protocol that allows the fetching of resources such as HTML documents

- Requests consist of 4 things

  - Method
  - Path
  - Version of the protocol
  - Headers

    ```HTTP
    GET / HTTP/1.1
    Host: alsdka
    Accept-Language: Eng
    ```

- Responses consist of 4 things aswell

  - Version of the protocol
  - Status Code
  - Status message
  - Headers

    ```HTTP
    HTTP/1.1 200 OK
    Date: asjkda
    Server: Apache
    Last-Modified: Tue, Dec 1970
    Etag: etc...
    ```

- There are 9 HTTP request methods, but the 4 big ones are

  - GET: used to get data
  - POST: usually used to create some new data
  - PUT: generally used for editing existing data on the server
  - DELETE: used to delete some existing data

- HTTP is a request-response protocol, where the client makes requests and the server sends responses
- HTTP is a text based protocol, making it easy to read and understand for humans
- HTTP requests must contain the verb/method (eg: GET) and the Path (eg: /about)
- HTTP requests aren't always to receive data, but sometimes to save data, like when we submit a form on a website. This is done via a POST instead of a GET
- Requests and responses both contain key-value based headers (eg: Accept-Language: fr, Content-Type: text/html, etc.)

#### URL

- URL's can be broken down into 6 basic parts

  - Protocol it was sent over
  - Domain (Or host)
  - Port
  - Resouce Path
  - Query Parameters
  - Anchor

    ```URL
      http://www.example.edu.80/path/to/myfile.html?ker1=value1&key2=value2#Somewhere
    ```
