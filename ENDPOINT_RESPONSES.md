# Endpoint Responses - Bank System

## Accounts

### GET /accounts
- 200: Accounts retrieved successfully
- 500: Internal server error

### GET /accounts/{id}
- 200: Account retrieved successfully
- 404: Account not found
- 500: Internal server error

### POST /accounts
- 201: Account created successfully
- 400: Invalid account information
- 409: Account already exists
- 500: Internal server error

### GET /accounts/{id}/balance
- 200: Balance retrieved successfully
- 404: Account not found
- 500: Internal server error

### DELETE /accounts/{id}
- 204: Account deleted successfully
- 404: Account not found
- 500: Internal server error

## Transactions

### POST /transactions/deposit
- 200: Deposit successful
- 400: Invalid amount
- 404: Account not found
- 422: Invalid transaction
- 500: Internal server error

### POST /transactions/withdraw
- 200: Withdrawal successful
- 400: Invalid amount
- 404: Account not found
- 422: Insufficient balance
- 500: Internal server error

### POST /transactions/transfer
- 200: Transfer successful
- 400: Invalid amount
- 404: Source or destination account not found
- 422: Insufficient balance
- 500: Internal server error

### GET /transactions
- 200: Transactions retrieved successfully
- 500: Internal server error

## Customers

### GET /customers
- 200: Customers retrieved successfully
- 500: Internal server error

### GET /customers/{id}
- 200: Customer retrieved successfully
- 404: Customer not found
- 500: Internal server error

### POST /customers
- 201: Customer created successfully
- 400: Invalid customer information
- 409: Customer already exists
- 500: Internal server error

### PUT /customers/{id}
- 200: Customer updated successfully
- 400: Invalid information
- 404: Customer not found
- 500: Internal server error

### DELETE /customers/{id}
- 204: Customer deleted successfully
- 404: Customer not found
- 500: Internal server error

## Global Error

All endpoints may return:

- 401: Unauthorized
- 403: Forbidden
- 429: Too Many Requests
