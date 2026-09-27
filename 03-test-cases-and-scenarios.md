# 03. Test Scenarios, Test Cases, and Test Design Methods

## 1. What is a Test Scenario?

A test scenario is a high-level description of a real business flow or user action that needs to be tested.

### Example

- User logs in and places an order
- User searches for a product and filters results
- User updates profile details

### Characteristics

- more business-focused
- not too detailed
- covers multiple steps or business flows

---

## 2. What is a Test Case?

A test case is a complete set of steps, input values, preconditions, expected results, and postconditions used to validate a specific behavior.

### Standard test case fields

- Test case ID
- Test case name
- Objective
- Preconditions
- Test data
- Steps
- Expected result
- Actual result
- Status

### Example test case

**Title:** Verify login with valid credentials

- Precondition: User is on login page
- Steps:
  1. Enter valid username
  2. Enter valid password
  3. Click Login
- Expected result: User is redirected to homepage and login succeeds

---

## 3. Difference Between Test Scenario and Test Case

| Test Scenario | Test Case |
| -- | -- |
| High-level business flow | Detailed execution steps |
| Example: login process | Example: enter valid username and click login |
| Broad coverage | Specific validation |

> A test scenario may generate multiple test cases.

---

## 4. Positive Testing

Positive testing verifies that the system behaves correctly for valid inputs and expected actions.

### Example

- login with valid username/password
- submit valid form data
- apply valid search filter

### Goal

Ensure that the product works as intended for valid use.

---

## 5. Negative Testing

Negative testing checks whether the system handles invalid, wrong, or unexpected input correctly.

### Example

- login with wrong password
- enter special characters in name field
- invalid email format
- empty mandatory field

### Goal

Ensure the system rejects invalid input gracefully and shows appropriate messages.

---

## 6. Boundary Value Analysis (BVA)

Boundary value analysis checks values at the edge of valid and invalid ranges.

### Example

If age must be 18 to 60:

- valid boundary values: 18, 60
- just below boundary: 17
- just above boundary: 61

> Boundary values often reveal defects that normal average values miss.

---

## 7. Equivalence Partitioning

Equivalence partitioning divides input data into groups that are expected to behave similarly.

### Example

For a field accepting 1 to 10:

- valid partition: 1 to 10
- invalid partition: below 1 and above 10

This helps reduce the number of test cases without losing coverage.

---

## 8. Decision Table Testing

Decision table testing is used when multiple conditions lead to multiple outcomes.

### Example

For login:

- if username valid and password valid → allow login
- if username valid and password invalid → show error
- if username invalid and password valid → show error
- if both invalid → show error

This method is useful for rules-based logic.

---

## 9. State Transition Testing

State transition testing validates behavior when an application moves from one state to another.

### Example

- user logged out → login → logged in → logout → logged out

This is useful in workflows like login, shopping cart, or approval systems.

---

## 10. Error Guessing

Error guessing is based on tester experience and intuition. The tester tries scenarios likely to fail.

### Example

- blank fields
- duplicate entries
- unsupported special characters
- wrong sequence of steps

---

## 11. Use Case Testing

Use case testing validates real-world user actions and end-to-end workflows.

### Example

User creates account, logs in, adds product to cart, makes payment, and receives confirmation.

---

## 12. Test Data

Test data is the input used during test execution. It may be:

- valid data
- invalid data
- boundary data
- empty data
- duplicate data

Good test cases depend on good test data.

---

## 13. Test Case Design Best Practices

- Write clear and simple steps
- Keep expected results explicit
- Cover both positive and negative scenarios
- Include boundary and invalid conditions
- Make cases reusable and traceable to requirements
- Avoid ambiguous language like “should work fine”

---

## 14. What is a Bug?

A bug or defect is any mismatch between expected behavior and actual behavior.

### Example

Expected: clicking Save saves the form
Actual: clicking Save does nothing

This must be reported as a defect.

---

## 15. Sample Interview Questions

### Q1. What is the difference between test scenario and test case?

Answer:

> A test scenario is a high-level business flow, while a test case is a detailed set of steps with inputs and expected results.

### Q2. What is positive testing?

Answer:

> Positive testing checks whether valid inputs and expected actions produce correct behavior.

### Q3. What is negative testing?

Answer:

> Negative testing ensures that invalid or unexpected inputs are handled properly and no incorrect behavior occurs.

### Q4. What is boundary value analysis?

Answer:

> Boundary value analysis validates values at the edge of valid and invalid ranges because defects often occur around boundaries.

---

## 16. Quick Revision Summary

- Test scenario = high-level flow
- Test case = detailed steps
- Positive testing checks correct behavior
- Negative testing checks invalid behavior
- Boundary value analysis focuses on edge conditions
- Equivalence partitioning reduces redundant testing
- Decision tables help with rule-driven logic

---

## Final Interview-Ready Answer

> A test scenario represents a user or business flow that needs validation, while a test case is the detailed execution step set that checks that flow. Good test cases include valid and invalid inputs, boundary conditions, expected results, and clear pass/fail criteria. This ensures functional correctness and reduces the chance of missing real defects.
