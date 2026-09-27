# 04. Types of Testing

## 1. Functional Testing

Functional testing checks whether each function of the software works according to the requirements.

### Examples

- login
- registration
- checkout
- search
- file upload

---

## 2. Non-Functional Testing

Non-functional testing checks quality attributes such as performance, usability, reliability, and security.

### Examples

- performance testing
- accessibility testing
- security testing
- usability testing

---

## 3. Smoke Testing

Smoke testing is a quick sanity check to confirm that the most important features of the build work before deeper testing begins.

### Example

- application launches
- login works
- homepage loads
- basic navigation works

> Smoke testing is shallow but fast. It helps decide whether a build is stable enough for further testing.

---

## 4. Sanity Testing

Sanity testing is a focused check performed after a small change to confirm that the changed behavior works without full regression.

### Example

A new bug fix for login is tested by checking the login flow only, not the whole application.

> Smoke is broad and shallow; sanity is narrow and deep.

---

## 5. Regression Testing

Regression testing checks whether a recent change has broken existing functionality.

### Common use cases

- bug fix
- new feature release
- code refactor
- compatibility update

### Typical examples

- existing login tests after code changes
- checkout flow after UI updates
- payment flow after backend fix

---

## 6. Retest

Retest means testing the same defect again after the developer fixes it.

### Difference between Retest and Regression

- Retest = verify a specific fixed bug
- Regression = ensure no other parts were affected

---

## 7. Exploratory Testing

Exploratory testing is unscripted testing where the tester learns the application while testing it and finds defects through investigation.

### Good for

- new features
- usability analysis
- discovering unexpected issues
- creative defect hunting

> Exploratory testing is very useful when requirements are changing or not fully defined.

---

## 8. Ad-hoc Testing

Ad-hoc testing is informal testing without planning or documentation. It is based on tester experience.

### Characteristics

- less structured
- quick checks
- useful for finding obvious defects fast

---

## 9. Usability Testing

Usability testing evaluates ease of use, navigation, and user experience.

### Checks

- whether users can understand the flow
- whether labels are clear
- whether pages are intuitive
- whether tasks can be completed easily

---

## 10. Compatibility Testing

Compatibility testing checks whether the application works across different environments.

### Examples

- browsers: Chrome, Edge, Firefox
- OS: Windows, Mac, Android, iOS
- devices: mobile, tablet, desktop

---

## 11. Performance Testing

Performance testing measures how the system behaves under load and stress.

### Subtypes

- Load testing
- Stress testing
- Volume testing
- Scalability testing

### Example

- 1000 users logging in simultaneously
- huge database load
- slow response times under stress

---

## 12. Security Testing

Security testing ensures that the application is protected against vulnerabilities.

### Examples

- SQL injection
- broken authentication
- session hijacking
- improper access control

---

## 13. Recovery Testing

Recovery testing checks whether the system can recover from failure.

### Example

- application crash recovery
- database connection failure recovery
- session recovery after restart

---

## 14. Unit Testing

Unit testing tests the smallest component of an application in isolation.

### Usually done by

- developers
- automation engineers

---

## 15. Integration Testing

Integration testing checks how different modules interact with each other.

### Example

- UI sending data to backend API
- payment module working with order module

---

## 16. System Testing

System testing validates the complete software system against the specified requirements.

### Focus

- end-to-end behavior
- overall product quality
- system interactions

---

## 17. User Acceptance Testing (UAT)

UAT is done by end users or business stakeholders to confirm that the product meets business needs and is ready for release.

### Goal

Check whether the solution is acceptable for real usage.

---

## 18. Alpha and Beta Testing

### Alpha Testing

Testing done internally by the development team or QA team before release.

### Beta Testing

Testing done by real users outside the organization to collect real-world feedback.

---

## 19. Black Box vs White Box Revisited

- Black box = testing based on input/output behavior
- White box = testing based on internal logic and code structure

---

## 20. Interview Questions and Answers

### Q1. What is smoke testing?

Answer:

> Smoke testing is a basic check of the critical functions of an application to confirm the build is stable enough for further testing.

### Q2. Difference between retest and regression testing?

Answer:

> Retest verifies a specific bug fix, whereas regression ensures that the fix did not break other existing functionality.

### Q3. What is exploratory testing?

Answer:

> Exploratory testing is learning and testing simultaneously, without a fixed script, to discover defects quickly and creatively.

### Q4. What is UAT?

Answer:

> UAT is performed by end users or business stakeholders to validate whether the software meets business expectations before release.

---

## 21. Quick Revision Summary

- Smoke = quick check of critical features
- Sanity = focused validation after small changes
- Regression = broad validation after changes
- Retest = confirm bug fix works
- Exploratory = free-form learning and testing
- Performance = speed, load, and stability
- UAT = business readiness check
- Security = protection against attacks

---

## Final Interview-Ready Answer

> Testing is not limited to one type. Functional testing validates business behavior, while non-functional testing ensures quality attributes such as performance, security, and usability. Smoke and sanity tests are quick checks, regression and retest cover change impact, and exploratory testing helps discover unexpected issues. Together they provide better product confidence before release.
