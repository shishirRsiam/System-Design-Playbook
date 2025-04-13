## 🔍 What is HTTP?

**HTTP (HyperText Transfer Protocol)** is the foundation of communication on the web. It’s how browsers (clients) talk to servers.

- The client sends an **HTTP request**.
- The server sends back an **HTTP response**.

Both requests and responses have:
- A **status line** (e.g., `HTTP/1.1 200 OK`)
- **Headers** (e.g., `Content-Type: application/json`)
- An optional **body** (e.g., JSON data)

---

## 📋 Common HTTP Methods

| Method | Description |
|--------|-------------|
| `GET`    | Retrieve data (e.g., fetch posts) |
| `POST`   | Send data to the server (e.g., submit form) |
| `PUT`    | Update/replace data |
| `PATCH`  | Partially update data |
| `DELETE` | Delete data |
| `HEAD`   | Like `GET`, but without the response body |
| `OPTIONS`| Describes the allowed methods |

---

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