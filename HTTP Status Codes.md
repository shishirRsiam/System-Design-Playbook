
## 🟢 HTTP Status Codes (Grouped)

### ✅ 1xx – Informational
- **100 Continue** – Everything is OK so far.
- **101 Switching Protocols** – Server is switching protocols (e.g., HTTP to WebSockets).

### 🟢 2xx – Success
- **200 OK** – Request succeeded.
- **201 Created** – Resource created (common with POST).
- **202 Accepted** – Request accepted but not completed.
- **204 No Content** – Success, but no content to return.

### 🟡 3xx – Redirection
- **301 Moved Permanently** – Resource moved; update your URL.
- **302 Found** – Temporarily moved.
- **304 Not Modified** – Use cached version.

### 🔴 4xx – Client Errors
- **400 Bad Request** – Invalid input.
- **401 Unauthorized** – Need login/authentication.
- **403 Forbidden** – Authenticated but not allowed.
- **404 Not Found** – Resource doesn’t exist.
- **405 Method Not Allowed** – Method not allowed (e.g., using POST where only GET is allowed).
- **429 Too Many Requests** – Rate limit exceeded.

### 🔴 5xx – Server Errors
- **500 Internal Server Error** – Server crashed or error occurred.
- **502 Bad Gateway** – Server received an invalid response from another server.
- **503 Service Unavailable** – Server is down/overloaded.
- **504 Gateway Timeout** – Timeout between servers.

---
---


Here's a **complete and detailed list of all HTTP status codes**, grouped by category with descriptions for each one. You don’t need to memorize all, but understanding the most used ones is essential. You can always refer back to this when needed.

---

## ✅ **1xx: Informational**  
These mean the request was received and the process is continuing.

| Code | Meaning                      | Description |
|------|------------------------------|-------------|
| 100  | Continue                     | Client should continue the request. |
| 101  | Switching Protocols          | Server is switching protocols (e.g., to WebSocket). |
| 102  | Processing (WebDAV)          | Server has received the request and is working on it. |
| 103  | Early Hints                  | Used for preloading resources before final response. |

---

## 🟢 **2xx: Success**  
These mean the action was successfully received and understood.

| Code | Meaning                      | Description |
|------|------------------------------|-------------|
| 200  | OK                           | Standard response for successful requests. |
| 201  | Created                      | Resource successfully created (commonly POST). |
| 202  | Accepted                     | Request accepted, processing not completed. |
| 203  | Non-Authoritative Information | Response from a third party (not original server). |
| 204  | No Content                   | Success but no content returned. |
| 205  | Reset Content                | Tell the user to reset the view (form cleared). |
| 206  | Partial Content              | Partial response (used in file downloads, range). |
| 207  | Multi-Status (WebDAV)        | Multiple status codes for multiple resources. |
| 208  | Already Reported (WebDAV)    | Elements already reported earlier. |
| 226  | IM Used                      | Server has fulfilled a request using a transformation (rare). |

---

## 🟡 **3xx: Redirection**  
Client must take additional action to complete request.

| Code | Meaning                      | Description |
|------|------------------------------|-------------|
| 300  | Multiple Choices             | Multiple options (rarely used). |
| 301  | Moved Permanently            | Resource moved, update your URL. |
| 302  | Found                        | Temporary redirect (commonly used). |
| 303  | See Other                    | Redirect to another resource (GET). |
| 304  | Not Modified                 | Cached version is valid. |
| 305  | Use Proxy                    | Deprecated, use proxy to access resource. |
| 306  | Switch Proxy                 | No longer used. |
| 307  | Temporary Redirect           | Like 302 but method remains unchanged. |
| 308  | Permanent Redirect           | Like 301 but method remains unchanged. |

---

## 🔴 **4xx: Client Errors**  
The client seems to have made a mistake.

| Code | Meaning                      | Description |
|------|------------------------------|-------------|
| 400  | Bad Request                  | Malformed syntax or invalid request. |
| 401  | Unauthorized                 | Authentication required. |
| 402  | Payment Required             | Reserved for future use. |
| 403  | Forbidden                    | Authenticated but not allowed. |
| 404  | Not Found                    | Resource doesn't exist. |
| 405  | Method Not Allowed           | Method not allowed on resource (e.g. GET vs POST). |
| 406  | Not Acceptable               | Resource can't be returned in requested format. |
| 407  | Proxy Authentication Required | Must authenticate with a proxy. |
| 408  | Request Timeout              | Client took too long to send request. |
| 409  | Conflict                     | Conflict with current state of resource. |
| 410  | Gone                         | Resource permanently removed. |
| 411  | Length Required              | Missing `Content-Length` header. |
| 412  | Precondition Failed          | Preconditions in headers failed. |
| 413  | Payload Too Large            | Body is too large. |
| 414  | URI Too Long                 | URL is too long to process. |
| 415  | Unsupported Media Type       | Format of request not supported. |
| 416  | Range Not Satisfiable        | Client asked for range not valid for resource. |
| 417  | Expectation Failed           | Server can’t meet the requirements of Expect header. |
| 418  | I'm a teapot 🫖              | Joke from [RFC 2324](https://datatracker.ietf.org/doc/html/rfc2324) (used in fun APIs). |
| 421  | Misdirected Request          | Request was directed at the wrong server. |
| 422  | Unprocessable Entity         | Semantic errors (e.g., validation failed). |
| 423  | Locked                       | Resource is locked. |
| 424  | Failed Dependency            | Dependent request failed. |
| 425  | Too Early                    | Server is unwilling to risk processing. |
| 426  | Upgrade Required             | Client should switch to a different protocol. |
| 428  | Precondition Required        | Server requires preconditions. |
| 429  | Too Many Requests            | Client is sending requests too fast (rate limit). |
| 431  | Request Header Fields Too Large | Headers are too large. |
| 451  | Unavailable For Legal Reasons | Blocked due to legal reasons. |

---

## 🔴 **5xx: Server Errors**  
The server messed up.

| Code | Meaning                      | Description |
|------|------------------------------|-------------|
| 500  | Internal Server Error        | Generic server error. |
| 501  | Not Implemented              | Server doesn’t support requested method. |
| 502  | Bad Gateway                  | Invalid response from upstream server. |
| 503  | Service Unavailable          | Server is temporarily down. |
| 504  | Gateway Timeout              | Upstream server timed out. |
| 505  | HTTP Version Not Supported   | HTTP version not supported by server. |
| 506  | Variant Also Negotiates      | Configuration error. |
| 507  | Insufficient Storage         | Server is out of space (WebDAV). |
| 508  | Loop Detected                | Infinite loop in request (WebDAV). |
| 510  | Not Extended                 | Further extensions required. |
| 511  | Network Authentication Required | Authenticate to access network. |

---

## 📌 Tips to Remember
- **200 OK**, **201 Created**, **204 No Content** → Common in successful API usage.
- **400 Bad Request**, **401 Unauthorized**, **403 Forbidden**, **404 Not Found** → Common client errors.
- **500 Internal Server Error**, **502**, **503** → Typical server-side issues.

