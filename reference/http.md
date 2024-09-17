# HTTP

HTTP is a communication protocol designed for the web.

- [Primary reference on HTML](https://developer.mozilla.org/en-US/docs/Web/HTTP)


## Basic example

### Request

```http
GET / HTTP/1.1
Host: developer.mozilla.org
Accept-Language: fr
```

### Response

```http
HTTP/1.1 200 OK
Date: Sat, 09 Oct 2010 14:28:02 GMT
Server: Apache
Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
ETag: "51142bc1-7449-479b075b2891b"
Accept-Ranges: bytes
Content-Length: 29769
Content-Type: text/html

<html></html>
```
