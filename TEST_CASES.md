# Test Cases - Bank System

## Deposit Tests

| ID | Test Scenario | Expected Status Code | Expected Result |
|---|---|---|---|
| TC-01 | Deposit with valid amount | 200 | Deposit successful |
| TC-02 | Deposit with negative amount | 400 | Invalid amount |
| TC-03 | Deposit with zero amount | 400 | Invalid amount |

## Withdraw Tests

| ID | Test Scenario | Expected Status Code | Expected Result |
|---|---|---|---|
| TC-04 | Withdraw with valid amount | 200 | Withdrawal successful |
| TC-05 | Withdraw with insufficient balance | 400 | Insufficient funds |
| TC-06 | Withdraw with negative amount | 400 | Invalid amount |

## Transfer Tests

| ID | Test Scenario | Expected Status Code | Expected Result |
|---|---|---|---|
| TC-07 | Transfer with valid amount | 200 | Transfer successful |
| TC-08 | Transfer to invalid account | 404 | Account not found |
| TC-09 | Transfer with insufficient balance | 400 | Insufficient funds |
