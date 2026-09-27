# 01. Manual Testing Fundamentals

## 1. What is Manual Testing?

Manual testing is the process of manually checking software applications to identify defects, validate behavior, and ensure that the product meets requirements. A tester performs the application steps by step, compares actual output with expected output, and reports defects.

### Example

If a login page is expected to accept valid credentials and reject invalid ones, the tester manually checks:

- valid username + valid password → login successful
- valid username + wrong password → error message displayed
- blank username/password → validation message shown

---

## 2. Why is Manual Testing Needed?

Manual testing is important because it validates:

- user experience
- UI behavior
- usability and readability
- exploratory scenarios
- business flows that automation cannot fully capture at early stages

> Manual testing is especially valuable in early product validation, usability testing, and when requirements are changing frequently.

---

## 3. Difference Between QA, QC, and Testing

### Quality Assurance (QA)

QA is a process-oriented approach that ensures the product is built in the right way. It focuses on preventing defects by improving processes.

### Quality Control (QC)

QC is product-oriented and checks whether the product meets specified requirements.

### Testing

Testing is the execution of test cases to find defects and validate quality.

### Simple Example

- QA = process to reduce mistakes
- QC = checking the final product
- Testing = running the product to check if it works

---

## 4. Verification vs Validation

### Verification

Verification answers: Are we building the product right?

- review of requirements
- walkthroughs
- inspections
- design review

### Validation

Validation answers: Are we building the right product?

- executing the software
- checking actual output vs expected output
- user acceptance validation

> Verification is process-focused; validation is product-focused.

---

## 5. Manual Testing vs Automation Testing

| Aspect | Manual Testing | Automation Testing |
| -- | -- | -- |
| Execution | Human-driven | Script-driven |
| Best for | Exploratory, UI, UX, UAT | Regression, repeated checks |
| Speed | Slower | Faster for repetitive tasks |
| Cost | Lower initial cost | Higher initial setup cost |
| Reusability | Low | High |

> Manual testing is best for discovery and exploratory coverage, whereas automation is best for repeated execution and regression validation.

---

## 6. Black Box Testing

Black box testing focuses on the external behavior of the application without looking into internal code.

### Examples

- login page validation
- search functionality
- payment flow
- form submission

### Characteristics

- tester does not need coding knowledge
- tests based on requirements
- checks user-visible behavior

---

## 7. White Box Testing

White box testing is done with knowledge of internal logic, code structure, and design.

### Common examples

- unit testing
- code path validation
- logic branch testing
- path coverage

### Suitable for

- developers
- automation engineers
- code-level validation

> White box testing is more technical and focuses on internal implementation correctness.

---

## 8. Grey Box Testing

Grey box testing is a combination of black box and white box testing. The tester has partial knowledge of internal code and tests based on both functionality and internal design.

### Common use cases

- integration testing
- database validation
- API workflow checks

---

## 9. Test Objective

The main objectives of testing are to:

- detect defects early
- reduce risk
- improve quality
- ensure requirements are met
- verify software is usable and stable

---

## 10. Principles of Testing

The key testing principles are:

1. Testing shows presence of defects, not absence of defects.
2. Exhaustive testing is impossible.
3. Early testing saves time and cost.
4. Defect clustering means a small subset of modules often contains most defects.
5. Pesticide paradox means repeating the same tests may not find new bugs.
6. Testing depends on context.
7. Absence-of-errors is a fallacy if the product does not meet user needs.

> These principles are essential interview answers and are frequently asked in QA interviews.

---

## 11. Test Levels

Testing is organized into levels:

- Unit testing
- Integration testing
- System testing
- Acceptance testing

### Unit Testing
Tests individual components or functions.

### Integration Testing
Checks interaction between modules.

### System Testing
Validates the whole application against system requirements.

### Acceptance Testing
Ensures the product is acceptable to the business or end user.

---

## 12. Real Interview Points

### Common interview question

What is manual testing?

Answer:

> Manual testing is the process of validating the software by executing test cases manually to check whether the actual result matches the expected result and to identify defects.

### Another common question

What is the difference between black box and white box testing?

Answer:

> Black box testing checks the external behavior of the application without knowing internal code, whereas white box testing validates internal logic and code structure.

---

## 13. Quick Revision Summary

- Manual testing is a human-driven validation process.
- Testing helps detect defects and improve quality.
- QA is process-focused; QC is product-focused.
- Verification checks if we are building right; validation checks if we are building the right thing.
- Black box, white box, and grey box cover different testing approaches.

---

## Short Interview Answer

> Manual testing is the process of evaluating software manually to find defects, check whether functionality matches requirements, and validate usability and business flow before release. It is essential for exploratory testing, UI validation, and user-centric quality checks.
