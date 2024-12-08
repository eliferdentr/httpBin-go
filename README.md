# httpBin-go
 HTTPBin project backend written using Go
API Design
1. GET /get
Description: Tests HTTP GET requests.
Parameters:
query (optional): Returns any query parameters sent with the request.
Response:
{
  "url": "https://example.com/get",
  "headers": { "Content-Type": "application/json" },
  "args": { "key": "value" },
  "origin": "192.168.1.1"
}
2. POST /post
Description: Tests HTTP POST requests.
Parameters:
Body data (JSON, form-data, or raw).
Response:
{
  "url": "https://example.com/post",
  "headers": { "Content-Type": "application/json" },
  "data": { "name": "John Doe" },
  "origin": "192.168.1.1"
}
3. PUT /put
Description: Tests HTTP PUT requests.
Parameters:
Body data (JSON, form-data, or raw).
Response:
{
  "url": "https://example.com/put",
  "headers": { "Content-Type": "application/json" },
  "data": { "key": "updated value" },
  "origin": "192.168.1.1"
}
4. DELETE /delete
Description: Tests HTTP DELETE requests.
Response:
{
  "url": "https://example.com/delete",
  "headers": { "Content-Type": "application/json" },
  "origin": "192.168.1.1",
  "message": "Resource deleted"
}
5. /headers
Description: Returns HTTP headers sent with the request.
Response:
{
  "headers": {
    "User-Agent": "PostmanRuntime/7.29.0",
    "Accept": "*/*",
    "Cache-Control": "no-cache"
  }
}
6. /ip
Description: Returns the client's IP address.
Response:
{
  "origin": "192.168.1.1"
}
7. /status/:code
Description: Returns a specific HTTP status code.
Parameters:
code: The HTTP status code to return (e.g., 200, 404, 500).
Response:
{
  "status": "Status code: 404"
}
8. /delay/:seconds
Description: Delays the response.
Parameters:
seconds: The delay time in seconds.
Response:
{
  "message": "Response delayed by 5 seconds"
}
