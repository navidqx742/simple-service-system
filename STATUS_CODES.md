# Status Codes - Bank System

## HTTP Status Codes

| Status Code | Meaning | When to Use |
|---|---|---|
| 200 | OK | Request successful |
| 201 | Created | Account or customer created |
| 204 | No Content | Resource deleted successfully |
| 400 | Bad Request | Invalid request data |
| 401 | Unauthorized | User is not authenticated |
| 403 | Forbidden | User has no permission |
| 404 | Not Found | Account or customer not found |
| 409 | Conflict | Duplicate account or conflict |
| 422 | Unprocessable Entity | Invalid transaction data |
| 429 | Too Many Requests | Request limit exceeded |
| 500 | Internal Server Error | Unexpected server error |

## Error Response Examples

### 400 Bad Request

{
  "status": 400,
  "error": "Bad Request",
  "message": "Invalid amount. Amount must be greater than zero."
}

### 401 Unauthorized

{
  "status": 401,
  "error": "Unauthorized",
  "message": "Authentication is required."
}

### 403 Forbidden

{
  "status": 403,
  "error": "Forbidden",
  "message": "You do not have permission to perform this action."
}

### 404 Not Found

{
  "status": 404,
  "error": "Not Found",
  "message": "The requested account was not found."
}

### 409 Conflict

{
  "status": 409,
  "error": "Conflict",
  "message": "An account with this information already exists."
}

### 422 Unprocessable Entity

{
  "status": 422,
  "error": "Unprocessable Entity",
  "message": "Insufficient account balance for this transaction."
}

### 429 Too Many Requests

{
  "status": 429,
  "error": "Too Many Requests",
  "message": "You have exceeded your request limit.",
  "retry_after": 60
}

### 500 Internal Server Error

{
  "status": 500,
  "error": "Internal Server Error",
  "message": "An unexpected error occurred. Please try again later."
}
