
# HTTP Response Status Codes

## 1. Informational Responses (1xx)
| Code | Name | Description |
|---|---|---|
| 100 | Continue | The request can continue. |
| 101 | Switching Protocols | The server is switching protocols. |
| 102 | Processing | The server is processing the request. |
| 103 | Early Hints | Provides preliminary response information. |

## 2. Successful Responses (2xx)
| Code | Name | Description |
|---|---|---|
| 200 | OK | Request successful. |
| 201 | Created | Resource created successfully. |
| 202 | Accepted | Request accepted for processing. |
| 204 | No Content | Request successful, with no response body. |
| 206 | Partial Content | Partial resource returned. |

## 3. Redirection Messages (3xx)
| Code | Name | Description |
|---|---|---|
| 301 | Moved Permanently | Resource permanently moved. |
| 302 | Found | Temporary redirect. |
| 303 | See Other | Retrieve the resource from another URL. |
| 304 | Not Modified | Use the cached resource. |
| 307 | Temporary Redirect | Temporary redirect preserving the request method. |
| 308 | Permanent Redirect | Permanent redirect preserving the request method. |

## 4. Client Error Responses (4xx)
| Code | Name | Description |
|---|---|---|
| 400 | Bad Request | Invalid request. |
| 401 | Unauthorized | Authentication is required or has failed. |
| 403 | Forbidden | Access is denied. |
| 404 | Not Found | Resource not found. |
| 405 | Method Not Allowed | HTTP method is not supported for the resource. |
| 408 | Request Timeout | Request took too long. |
| 409 | Conflict | Request conflicts with the resource state. |
| 410 | Gone | Resource is no longer available. |
| 413 | Content Too Large | Request body exceeds the allowed limit. |
| 415 | Unsupported Media Type | Request format is not supported. |
| 422 | Unprocessable Content | Request content cannot be processed. |
| 429 | Too Many Requests | Too many requests were sent. |

## 5. Server Error Responses (5xx)
| Code | Name | Description |
|---|---|---|
| 500 | Internal Server Error | Unexpected server error. |
| 501 | Not Implemented | Functionality is not supported. |
| 502 | Bad Gateway | Invalid response from an upstream server. |
| 503 | Service Unavailable | Server is temporarily unavailable. |
| 504 | Gateway Timeout | Upstream server did not respond in time. |

## Example HTTP Response

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "message": "Request successful"
}
```

## Summary

- **1xx:** Informational
- **2xx:** Success
- **3xx:** Redirection
- **4xx:** Client errors
- **5xx:** Server errors

## References

- [MDN HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status)
- [IANA HTTP Status Code Registry](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
