# Automated-API-Testing-for-User-Authentication

This project contains Postman tests for **User Authentication API** using [Reqres](https://reqres.in).

## Files

1. **UserAuth_API_Test_With_Bonus.postman_collection.json** – Postman collection with 5 test cases:
   - Test Case 1: Valid login
   - Test Case 2: Invalid login (wrong email and password)
   - Test Case 3: Missing password
   - Test Case 4: Missing email
   - Test Case 5: Bonus – Data-driven login using CSV

2. **login_test_data.csv** – CSV file for Test Case 5 (Bonus) with different credentials.

---

## How to Run

### Using Postman

1. Open Postman → click **Import** → select `UserAuth_API_Test_With_Bonus.postman_collection.json`.
2. To run individual tests:
   - Select the test → click **Send**.
3. To run **data-driven tests** (Bonus):
   - Open **Collection Runner**.
   - Select the imported collection.
   - Click **Select File** → choose `login_test_data.csv`.
   - Click **Run**. Postman will iterate through all rows using the variables `{{email}}` and `{{password}}`.

### Assertions

- Status code verification (200 for valid, 400 for errors)
- Response content:
  - `token` for valid login
  - `error` for invalid or missing fields
