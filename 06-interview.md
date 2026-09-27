# 06. Manual Testing Interview Questions and Scenario-Based Answers

## 1. Basic Interview Questions

### Q1. What is Manual Testing?

Manual testing is the process of validating software by manually executing test cases to compare actual results with expected results and identify defects.

> Manual testing is important because it validates user behavior, usability, exploratory flows, and visual correctness that automation may not catch easily.

---

### Q2. What is the difference between QA and QC?

- QA is process-oriented and prevents defects.
- QC is product-oriented and detects defects.

> QA focuses on improving process quality; QC focuses on checking the final product.

---

### Q3. What is the difference between Verification and Validation?

- Verification = Are we building the product correctly?
- Validation = Are we building the right product?

Examples:
- Verification: code review, design review, requirement review
- Validation: testing the application behavior in real execution

---

### Q4. Why do we test software?

We test software to:

- find defects early
- reduce business risk
- ensure customer requirements are met
- improve quality and reliability
- verify usability and stability before release

---

## 2. SDLC and STLC Interview Questions

### Q5. What is SDLC?

SDLC is the complete process for developing software from requirement gathering to maintenance.

Common phases:
- Requirement Gathering
- Analysis
- Design
- Development
- Testing
- Deployment
- Maintenance

### Q6. What is STLC?

STLC is the testing lifecycle that ensures software quality. It moves through:

- Requirement Analysis
- Test Planning
- Test Case Development
- Environment Setup
- Test Execution
- Defect Tracking
- Test Closure

### Q7. Difference between Waterfall and Agile?

- Waterfall: sequential, rigid, requirements fixed upfront
- Agile: iterative, flexible, requirements can change during sprints

> Agile is preferred in fast-changing business environments because delivery is incremental and feedback is frequent.

### Q8. What is V-Model?

The V-model pairs every development phase with a testing phase. It ensures validation happens alongside development and catches defects early.

### Q9. What is Spiral Model?

The Spiral model is risk-driven and iterative. It repeats development cycles and includes risk analysis with each iteration, making it useful for complex and high-risk projects.

---

## 3. Testing Types Interview Questions

### Q10. What is Functional Testing?

Functional testing checks whether the software functions as expected based on requirements.

Examples:
- login
- registration
- payment processing
- add to cart

### Q11. What is Non-Functional Testing?

Non-functional testing checks quality characteristics such as performance, security, usability, and reliability.

Examples:
- page load time
- application stability
- security checks
- accessibility

### Q12. What is Smoke Testing?

Smoke testing is a quick build verification to confirm whether the critical features work before deeper testing starts.

Example checklist:
- app opens
- login works
- homepage loads
- basic navigation works

### Q13. What is Sanity Testing?

Sanity testing is a narrow, focused check after a small change or bug fix to confirm the corrected behavior works.

> Smoke is broad and shallow; sanity is narrow and deep.

### Q14. What is Regression Testing?

Regression testing checks whether a new change has broken existing features.

Examples:
- after bug fix
- after new feature addition
- after code refactor

### Q15. What is Retest?

Retest is executed after a defect is fixed to confirm the specific issue is resolved.

### Q16. What is Exploratory Testing?

Exploratory testing is when the tester simultaneously learns, designs, and executes tests without a strictly scripted path.

It is useful for:
- new feature validation
- usability issues
- hidden defects

### Q17. What is Ad hoc Testing?

Ad hoc testing is informal testing based on the tester’s intuition, without predefined test cases.

### Q18. What is Compatibility Testing?

Compatibility testing checks whether the application works across different browsers, OS, devices, and screen sizes.

### Q19. What is Performance Testing?

Performance testing measures the system's speed, responsiveness, and stability under load.

Subtypes:
- load testing
- stress testing
- scalability testing
- volume testing

### Q20. What is Security Testing?

Security testing verifies the application is protected against vulnerabilities like SQL injection, broken authentication, unauthorized access, and data leaks.

### Q21. What is Accessibility Testing?

Accessibility testing ensures the application can be used by people with disabilities, such as screen-reader users, keyboard-only users, and visually impaired users.

### Q22. What is Recovery Testing?

Recovery testing checks whether the system can recover from crashes, failures, or unexpected interruptions.

### Q23. What is UAT (User Acceptance Testing)?

UAT is performed by business users or end users to confirm the software meets their real-world expectations and business needs before release.

---

## 4. Test Case and Scenario Questions

### Q24. What is a Test Scenario?

A test scenario is a high-level business or user flow that needs to be tested.

Example:
- user logs in, adds product to cart, and makes payment

### Q25. What is a Test Case?

A test case is a detailed set of steps, inputs, and expected results used to validate a specific behavior.

### Q26. Difference between Test Scenario and Test Case?

- Scenario = broad flow
- Test case = detailed validation steps

> One scenario can lead to multiple test cases.

### Q27. What is a positive test case?

A positive test case checks whether valid input produces the expected result.

Example:
- valid username + valid password => login succeeds

### Q28. What is a negative test case?

A negative test case checks whether invalid input is handled gracefully.

Example:
- wrong password => error message shown

### Q29. What is boundary value testing?

Boundary value testing validates values at the edge of valid and invalid ranges.

Example:
- age field allowed 18 to 60
- test 17, 18, 59, 60, 61

### Q30. What is equivalence partitioning?

Equivalence partitioning divides inputs into groups that are expected to behave similarly, reducing unnecessary test cases.

### Q31. What is decision table testing?

Decision table testing is used for logic involving multiple conditions and outcomes.

### Q32. What is state transition testing?

State transition testing validates transitions between states, such as login/logout, pending/approved/rejected, or cart empty/cart filled.

### Q33. What is error guessing?

Error guessing is based on tester intuition and experience to identify possibly failing scenarios.

---

## 5. Defect and Bug Reporting Questions

### Q34. What is a defect?

A defect is a mismatch between expected and actual behavior.

### Q35. What is a bug report?

A bug report is a formal record of a defect with steps to reproduce, expected results, actual results, and supporting evidence.

### Q36. What is severity?

Severity describes the impact of the defect on business operations or system stability.

### Q37. What is priority?

Priority defines how quickly the bug should be fixed.

### Q38. Difference between severity and priority?

- Severity = impact
- Priority = urgency

> A cosmetic issue may have low severity but medium priority depending on release schedule.

### Q39. What is the defect life cycle?

A defect typically moves through:

New → Assigned → Open → In Progress → Fixed → Retest → Verified → Closed

It may also be reopened if the fix fails.

---

## 6. Scenario-Based Questions

### Scenario 1: Application login issue

A login page accepts valid credentials but fails for a user who has a password with an uppercase letter and a number.

How would you test this?

Answer:

- verify valid credential scenarios
- test lowercase, uppercase, mixed case, numeric inputs
- check password validation rules
- verify error message for invalid input
- test boundary cases and special characters

---

### Scenario 2: Payment page broken after release

The checkout page shows a payment option, but the Continue button fails after a new UI update.

What should you do?

Answer:

- perform smoke testing on checkout flow
- run regression on payment-related forms
- verify page element IDs and button behavior
- validate field validations and API response flow
- log a defect with steps, screenshot, and environment details

---

### Scenario 3: Search functionality is returning wrong products

The application filters products by category, but the search results show irrelevant items.

What kind of testing would you perform?

Answer:

- functional testing of search logic
- negative testing with invalid keywords
- boundary and equivalence partitioning for filters
- regression testing after code changes
- exploratory testing for unexpected combinations

---

### Scenario 4: Bug fix applied but the same issue still appears

Developer says the issue is fixed, but in QA it still fails.

What is your approach?

Answer:

- retest the specific defect
- check if the bug is reproducible in the right environment
- confirm test data and build version
- verify if the fix is incomplete or wrong
- raise a defect if still failing and request clarification

---

### Scenario 5: Application works in Chrome but fails in Edge

What kind of testing is this?

Answer:

This is compatibility testing, especially cross-browser validation.

Need to check:
- browser versions
- CSS differences
- JavaScript compatibility
- layout and rendering issues

---

### Scenario 6: Build is deployed and you have only 30 minutes before release

What testing would you do first?

Answer:

- smoke testing on critical user flows
- regression on high-risk modules
- sanity testing on changed areas
- check severity/priority of open defects
- decide if release is safe based on defect risk

---

## 7. Common Real-Time Interview Questions

### Q40. How do you decide whether to release a build?

Answer:

- check smoke results
- review critical defects and their severity
- ensure high-priority flows are passing
- confirm regression tests are stable
- assess business impact and stakeholder signoff

### Q41. How do you write a good test case?

Answer:

- include clear steps
- provide preconditions and test data
- state expected results
- keep it specific and reproducible
- ensure it matches the requirement

### Q42. How do you handle a defect that is not reproducible?

Answer:

- review steps carefully
- confirm environment and test data
- try again in the same conditions
- check if it is a configuration issue
- reject or escalate with evidence if not reproducible

### Q43. What is the difference between smoke and regression testing?

Answer:

- Smoke testing is a quick check of critical flows
- Regression testing is a broader validation to ensure old features are not broken

### Q44. What is the difference between smoke and sanity testing?

Answer:

- Smoke = quick build readiness
- Sanity = focused validation after a specific change

### Q45. What is the role of a QA engineer in Agile?

Answer:

- understand user stories
- write/execute test cases
- participate in sprint planning and daily standups
- report defects
- perform regression and acceptance checks
- validate business requirements in each sprint

---

## 8. Important Quick Notes for Interviews

- Always talk in terms of business value and user impact.
- Connect testing to real user flows.
- Explain the difference between each testing type clearly.
- Mention defects and bug reporting because this is a common interview topic.
- Show awareness of both manual and automated testing context.

---

## 9. Strong Final Answer for Manual Testing Interview

> Manual testing is the process of validating software behavior by executing tests manually, comparing actual results with expected results, and identifying defects before release. A good tester understands SDLC and STLC, writes effective test cases, uses both positive and negative scenarios, and performs smoke, sanity, regression, exploratory, and performance checks depending on the requirement. I also focus on defect reporting quality, severity and priority, and business impact so the team can fix critical issues before release.

---

## 10. Last-Minute Revision Checklist

Before the interview, revise:

- SDLC vs STLC
- Waterfall, V-Model, Spiral, Agile
- Functional vs Non-Functional testing
- Smoke, Sanity, Regression, Retest
- Test scenario vs test case
- Positive vs negative testing
- Boundary, equivalence, state transition, decision table
- Defect life cycle
- Severity vs priority
- Bug report structure
- UAT and real-user validation

This is enough for strong interview preparation.
