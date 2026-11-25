# User Request Quota - Bank System

## Rate Limits

| User Type | Requests Per Minute |
|---|---:|
| Guest | 20 |
| Normal User | 60 |
| Admin | 120 |

## Rate Limit Rules

- Each user has a request limit per minute.
- Requests are counted separately for each user.
- When the limit is exceeded, the API returns 429 Too Many Requests.
- The user can retry after the specified time.

## Example Response

HTTP Status: 429 Too Many Requests

{
  "error": "Too Many Requests",
  "message": "You have exceeded your request limit.",
  "retry_after": 60
}
