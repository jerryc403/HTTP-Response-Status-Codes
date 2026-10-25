HTTP Response Status Codes
Introduction

HTTP (Hypertext Transfer Protocol) response status codes are three-digit numbers returned by a server in response to a client's request. They indicate whether the request was successful, whether further action is needed, or whether an error occurred.

Status codes are grouped into five categories based on the first digit.

1. Informational Responses (1xx)

These codes indicate that the request was received and the process is continuing.

Status Code	Name	Description
100	Continue	The client can continue sending the request.
101	Switching Protocols	The server agrees to switch protocols.
102	Processing	The server is processing the request but has not completed it.
103	Early Hints	Provides preliminary information to help the client prepare for the final response.
2. Successful Responses (2xx)

These codes indicate that the request was successfully received, understood, and processed.

Status Code	Name	Description
200	OK	The request was successful.
201	Created	A new resource was successfully created.
202	Accepted	The request was accepted for processing but has not been completed.
203	Non-Authoritative Information	The response contains information from a modifying intermediary.
204	No Content	The request succeeded, but there is no response content.
205	Reset Content	The client should reset the document view or form.
206	Partial Content	The server returned part of the requested resource.
3. Redirection Messages (3xx)

These codes indicate that additional action is needed to complete the request, often by accessing another URL.

Status Code	Name	Description
300	Multiple Choices	Multiple possible responses are available.
301	Moved Permanently	The resource has permanently moved to a new URL.
302	Found	The resource is temporarily available at another URL.
303	See Other	The client should retrieve the response from another URL, typically using GET.
304	Not Modified	The resource has not changed since the client's last request.
307	Temporary Redirect	The resource is temporarily available at another URL, preserving the request method.
308	Permanent Redirect	The resource has permanently moved, preserving the request method.
4. Client Error Responses (4xx)

These codes indicate that the request has an issue, such as invalid data, missing authentication, or a resource that cannot be found.

Status Code	Name	Description
400	Bad Request	The server cannot process the request because it is invalid or malformed.
401	Unauthorized	Authentication is required or has failed.
403	Forbidden	The server refuses to fulfill the request.
404	Not Found	The requested resource could not be found.
405	Method Not Allowed	The HTTP method is not supported for the resource.
406	Not Acceptable	The server cannot provide a response matching the client's acceptable formats.
408	Request Timeout	The server timed out waiting for the request.
409	Conflict	The request conflicts with the current state of the resource.
410	Gone	The resource is no longer available and this is expected to be permanent.
413	Content Too Large	The request content exceeds the server's allowed limit.
414	URI Too Long	The requested URI is longer than the server will accept.
415	Unsupported Media Type	The request content format is not supported.
416	Range Not Satisfiable	The requested range of a resource cannot be provided.
422	Unprocessable Content	The request format is understood, but its instructions cannot be processed.
423	Locked	The resource is locked.
425	Too Early	The server is unwilling to process a request that might be replayed.
426	Upgrade Required	The client must switch to a different protocol.
428	Precondition Required	The server requires a conditional request.
429	Too Many Requests	The client has sent too many requests in a given period.
431	Request Header Fields Too Large	The request headers are too large to process.
451	Unavailable For Legal Reasons	Access to the resource is denied for legal reasons.
5. Server Error Responses (5xx)

These codes indicate that the server failed to fulfill an apparently valid request.

Status Code	Name	Description
500	Internal Server Error	An unexpected error occurred on the server.
501	Not Implemented	The server does not support the functionality required to fulfill the request.
502	Bad Gateway	The server received an invalid response from an upstream server.
503	Service Unavailable	The server is temporarily unable to handle the request.
504	Gateway Timeout	The server did not receive a timely response from an upstream server.
505	HTTP Version Not Supported	The server does not support the HTTP version used in the request.
507	Insufficient Storage	The server cannot store the information needed to complete the request.
508	Loop Detected	The server detected an infinite loop while processing the request.
510	Not Extended	Further extensions to the request are required.
511	Network Authentication Required	The client must authenticate to gain network access.
Common HTTP Status Codes to Remember

The following codes are especially common in web development and API testing:

200 OK — Request successful.
201 Created — Resource created successfully.
204 No Content — Successful request with no response body.
301 Moved Permanently — Permanent redirect.
302 Found — Temporary redirect.
304 Not Modified — Cached resource can be reused.
400 Bad Request — Invalid request.
401 Unauthorized — Authentication required or failed.
403 Forbidden — Access denied.
404 Not Found — Resource not found.
405 Method Not Allowed — Unsupported HTTP method for the resource.
409 Conflict — Conflict with the resource's current state.
422 Unprocessable Content — Request content cannot be processed.
429 Too Many Requests — Rate limit exceeded.
500 Internal Server Error — Unexpected server error.
502 Bad Gateway — Invalid upstream response.
503 Service Unavailable — Server temporarily unavailable.
504 Gateway Timeout — Upstream server timed out.
Example HTTP Response

An HTTP response typically contains a status line, headers, a blank line, and optionally a response body.

http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "message": "Request successful"
}


In this example:

HTTP/1.1 is the HTTP protocol version.
200 is the status code.
OK is the reason phrase.
Content-Type indicates the format of the response body.
The JSON object contains the response data.
Conclusion

HTTP response status codes help clients and servers communicate the outcome of requests. Understanding these codes makes it easier to troubleshoot errors, develop APIs, test applications, and diagnose network problems.

Remember the five main categories:

1xx: Informational
2xx: Success
3xx: Redirection
4xx: Client errors
5xx: Server errors

For the official reference, visit the IANA HTTP Status Code Registry or the MDN HTTP response status codes guide.
