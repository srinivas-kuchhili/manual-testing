## 1. What is Manual Testing?
> Manual testing is the process of testing software or an application manually, again and again, to find defects according to customer requirements.

# Content of Manual Testing

1. SDLC (Software Development Life Cycle)
2. Software Testing
3. Test Cases
4. STLC (Software Testing Life Cycle)
5. Test Plan
6. Defect Life Cycle
7. ISTQB Questions

---

## 2. SDLC (Software Development Life Cycle)
Definition: SDLC is a step-by-step or standard procedure used to develop a new software product.

## Types of SDLC Models
1. Waterfall Model
2. Spiral Model
3. V & V Model
4. Prototype Model
5. Derived Model
6. Hybrid Model
7. Agile Model

### Waterfall Model
Waterfall model is a step-by-step procedure or standard approach to develop new software.

#### Stages
- Requirement Collection
  - Feasibility Study
    - Design
      - Coding
        - Testing
          - Installation
            - Maintenance

#### Spiral Model
The Spiral model is a risk-driven SDLC model where the project repeatedly passes through planning, risk analysis, engineering, and evaluation in iterative cycles.

```mermaid
flowchart LR
    A[Requirements] --> B[Planning]
    B --> C[Risk Analysis]
    C --> D[Engineering / Development]
    D --> E[Testing]
    E --> F[Evaluation]
    F --> G{Customer Feedback?}
    G -->|Yes| B
    G -->|No| H[Release]
```

#### V and V Model
The V-model shows verification and validation activities aligned with each development phase. Each stage of development has a corresponding testing stage.

```mermaid
flowchart LR
    A[Requirements] --> B[System Design]
    B --> C[Architecture Design]
    C --> D[Module Design]
    D --> E[Coding]

    A1[Requirement Testing] --> A
    B1[System Testing] --> B
    C1[Integration Testing] --> C
    D1[Unit Testing] --> D

    E --> E1[Acceptance Testing]
    E1 --> F[Final Product]
```

#### Agile Model
- Agile is an iterative and incremental approach where the customer keeps changing requirements. Since the company is flexible, it accepts these changes, develops them, tests them, and delivers quality software to the customer in a short span of time. This is called Agile.

#### Principles of Agile / Advantages
- Customer can change the requirement at any stage of development.
- There is good communication among the customer, BA, developer, and test engineer.
- Releases should be very short.
- Our highest priority is customer satisfaction through quick delivery.
- The software is a very simple model to follow.
- Teams are self-organized.
- Developers, testers, and BAs have regular meetings, which help improve the process.

#### Scrum Model
- Scrum is a standard procedure that helps a team work together and develop new software.

#### Agile Terminologies
1. **Release**: A combination of sprints is called a release.
2. **Epic**: A complete set of requirements is called an epic.
3. **User Story**: A story is a feature, functionality, or module.
4. **Story Point**: Story point is a rough estimate given by developers and test engineers to develop and test each individual story.
5. **Swag**: Swag is a rough estimate given by developers and test engineers to develop and test each individual story in terms of hours.
6. **Sprint**: A sprint is the actual time spent by developers and test engineers to develop and test one or more stories.

#### Scrum Meetings / Scrum Ceremonies
1. **Sprint Planning**: Sprint Planning is a Scrum event where the Scrum Team collaboratively decides what work will be completed during the upcoming Sprint and creates a plan for delivering it.
   - Reviews and discusses Product Backlog Items/User Stories.
   - Clarifies requirements and acceptance criteria.
   - Selects the work that can realistically be completed in the Sprint.
   - Breaks stories into tasks where appropriate.
   - Estimates the work and identifies dependencies or risks.
   - Defines the Sprint Goal.

2. **Scrum Meeting / Daily Scrum / DSM**: Daily Scrum is a short, daily Scrum event where developers inspect progress toward the Sprint Goal and identify any impediments or adjustments needed to achieve it. Typical discussion:
   - What did I complete yesterday?
   - What am I planning to work on today?
   - Do I have any blockers or impediments?

3. **Sprint Retrospective Meeting**: Sprint Retrospective is a Scrum event held at the end of a Sprint where the Scrum Team reflects on how the Sprint went and identifies improvements to make in the next Sprint. The team typically discusses:
   - What went well?
   - What did not go well?
   - What can we improve?
   - What action items should we take?

4. **Release Retrospective Meeting**: A Release Retrospective is a meeting held after a major release to review the overall release process, identify what went well and what could be improved, and define actions for future releases. The team might identify:
   - Regression took too long.
   - Some requirements changed late.
   - Automation reduced manual testing effort.
   - Production defects occurred because of missing test coverage.

5. **Bug Triage / Defect Triage Meeting**: Bug or Defect Triage is a meeting where reported defects are reviewed, analyzed, prioritized, assigned, and tracked based on severity, impact, and business priority.

6. **Backlog Grooming / Backlog Refinement**: Backlog Refinement is an ongoing activity where the Scrum Team reviews and prepares upcoming Product Backlog Items so they are sufficiently understood, appropriately sized, and ready for future Sprints. During refinement:
   - Requirements are discussed.
   - User stories are clarified.
   - Acceptance criteria are reviewed.
   - Dependencies are identified.
   - Stories may be split into smaller stories.
   - Estimates are discussed.
   - Questions and ambiguities are resolved.
   - Items may be reordered based on product needs.

---

## 3. Software Testing
- The process of identifying or catching defects in software is called software testing.

## Types of Software Testing
1. White Box Testing
   1. Path Testing
   2. Conditional Testing
   3. Loop Testing
   4. Unit Testing
   5. Testing the code from a memory perspective
   6. Testing the code from a performance perspective

2. Black Box Testing
   1. Functional Testing
   2. Integration Testing
   3. System Testing
   4. Acceptance Testing
   5. Smoke Testing
   6. Adhoc Testing
   7. Globalization Testing
   8. Compatibility Testing
   9. Exploratory Testing
   10. Usability Testing
   11. Regression Testing

### White Box Testing
- Testing each and every line of code is called White Box Testing (WBT).

#### 1. Path Testing
- Here the developer writes the flowchart and tests each individual path.

#### 2. Conditional Testing
- Here the developer tests the code for both true and false logical conditions.

#### 3. Loop Testing
- Here the developer tests the loop and ensures it repeats for the defined number of cycles.

#### 4. Unit Testing
- The customer provides the requirement. The developer writes the main program and the corresponding test program in the same language. The test program runs against the main program and gives the result as pass or fail.

### Black Box Testing
- Testing or verifying the functionality or behavior of an application or software against the customer requirement specification is called Black Box Testing.

#### 1. Functional Testing
- Testing each and every component of the application rigorously and thoroughly against the customer requirement specification is called functional testing.
  1. Over Testing / Exhaustive Testing
     - Testing each and every component of an application by entering data that does not make sense.

  2. Under Testing
     - Testing each and every component of an application by entering an insufficient set of data is called under testing.

  3. Optimized Testing
     - Testing each and every component by entering data that makes sense is called optimized testing.

#### 2. Integration Testing
- Testing the data flow or interface between two or more modules/features is called integration testing.
  1. Incremental Integration Testing
     - Incrementally adding the modules and testing the data flow between them is called incremental integration testing.

  2. Non-Incremental Testing
     - Here we combine all modules in one shot and test the data flow between them. This is called non-incremental integration testing.

#### 3. System Testing
- It is an end-to-end testing done by the test engineer in a testing server/environment similar to the production server/environment.

#### 4. Acceptance Testing
- It is end-to-end testing done by end-users/customers where they use the software in real-time business for a particular period to check whether the software can handle all business scenarios and situations.
  1. User Acceptance Testing
  2. Operational Acceptance Testing
  3. Contract Acceptance Testing
  4. Compliance Acceptance Testing
  5. Beta Acceptance Testing

#### 5. Smoke Testing
- Testing the basic and critical features of an application before doing thorough or rigorous testing is called smoke testing.
  1. Formal Smoke Testing
     - The development lead sends a build to testing, the TL assigns the feature to the TE, and asks them to perform smoke testing and prepare a report.

  2. Informal Smoke Testing
     - The TL assigns a feature to the tester, but does not ask the tester to prepare a smoke test report.

#### 6. Adhoc Testing
- Testing the software randomly without looking into the requirements is called Adhoc testing.
  1. Buddy Testing - [Dev and TE]
  2. Pair Testing - [Tester and TE]
  3. Monkey Testing - [TE]

#### 7. Globalization Testing
1. I18N Testing
   - Testing the software developed for different languages is called I18N testing.

2. L10N Testing
   - Testing the software to check whether the application is developed according to country standards and culture is called L10N testing.

#### 8. Compatibility Testing
- Testing the functionality of an application or software for different hardware and software configurations is called compatibility testing.
  1. Hardware Compatibility Testing
  2. Software Compatibility Testing

#### 9. Exploratory Testing
- Understand the application, identify all possible scenarios, document them, and test the application by referring to the document. This is called exploratory testing.

#### 10. Usability Testing
- Testing the user-friendliness of an application is called usability testing.
  1. Yellow Box Testing
  2. GUI Testing
  3. Accessibility Testing

#### 11. Regression Testing
- Testing unchanged/old features to ensure that changes such as adding, removing, modifying, or fixing defects do not introduce new defects in unchanged/old features is called regression testing.
  1. Unit Regression Testing
     - Testing only the changes or modifications done by developers is called unit regression testing.

  2. Regional Regression Testing
     - Testing the changes and impacted/affected areas is called regional regression testing.

  3. Full Regression Testing

---

## 4. STLC (Software Test Life Cycle)
- STLC is a step-by-step or standard procedure to test a new software application.

- System study (understand the requirement)
- Write test plan
- Write test case
- Prepare Traceability Matrix
- Test case execution
- Defect tracking
- Prepare test case execution report
- Postmortem / Project Closure / Retrospective meeting

---

## 5. Test Plan
- A test plan is a document that drives all future testing activities.

#### Test Plan Consists of 15 Stages
- Objective
- Scope
- Test Methodology
- Test Approach
- Assumptions
- Risk
- Backup Plan
- Roles and Responsibilities
- Scheduling
- Defect Tracking
- Test Environment
- Entry and Exit Criteria
- Test Automation
- Deliverables
- Templates

## Test Cases
1. **Test Scenario**: A test scenario is a high-level description of a real business flow or user action that needs to be tested.

### Example
- User logs in and places an order.
- User searches for a product and filters results.
- User updates profile details.

2. **Test Case**: A test case is a complete set of steps, input values, preconditions, expected results, and postconditions used to validate a specific behavior.

### Standard Test Case Fields
- Test Case ID
- Test Case Name
- Objective
- Preconditions
- Test Data
- Steps
- Expected Result
- Actual Result
- Status
- Test Case Type
- Post Conditions
- Severity

### Example Test Case
**Title:** Verify login with valid credentials

- Precondition: User is on the login page
- Steps:
  1. Enter valid username
  2. Enter valid password
  3. Click Login
- Expected result: The user is redirected to the homepage and login succeeds.

---

## 6. Difference Between Test Scenario and Test Case

| Test Scenario | Test Case |
| --- | --- |
| High-level business flow | Detailed execution steps |
| Example: login process | Example: enter valid username and click login |
| Broad coverage | Specific validation |

> A test scenario may generate multiple test cases.

---

## 7. Positive Testing

Positive testing verifies that the system behaves correctly for valid inputs and expected actions.

### Example
- Login with valid username/password
- Submit valid form data
- Apply valid search filter

### Goal
Ensure that the product works as intended for valid use.

---

## 8. Negative Testing

Negative testing checks whether the system handles invalid, wrong, or unexpected input correctly.

### Example
- Login with wrong password
- Enter special characters in a name field
- Invalid email format
- Empty mandatory field

### Goal
Ensure the system rejects invalid input gracefully and shows appropriate messages.

---

### Test Case Design Techniques
1. Error Guessing
2. Equivalence Partitioning
3. Boundary Value Analysis (BVA)
4. Decision Table Technique
5. State Transition Diagram

1. **Error Guessing**: Error guessing is based on tester experience and intuition. The tester tries scenarios likely to fail.
   - Blank fields
   - Duplicate entries
   - Unsupported special characters
   - Wrong sequence of steps

2. **Equivalence Partitioning**: Equivalence partitioning divides input data into groups that are expected to behave similarly.
   1. Pressman Rule
   2. Practice Method

   ### Pressman Rule
   1. <Rule 1>: If the input is a range of values, design test cases for one valid and two invalid values.
   2. <Rule 2>: If the input is a set of values, design test cases for one valid and two invalid values.
   3. <Rule 3>: If the input is boolean, design test cases for both true and false values.

   ### Practice Method
   - If the input is a range of values, divide the range into equal parts and test all those values; also test at least two invalid values. This is called the practice method.

3. **Boundary Value Analysis (BVA)**: Boundary value analysis checks values at the edge of valid and invalid ranges.

### Example
If age must be 18 to 60:
- Valid boundary values: 18, 60
- Just below boundary: 17
- Just above boundary: 61

> Boundary values often reveal defects that normal average values miss.

## 9. Decision Table Testing

Decision table testing is used when multiple conditions lead to multiple outcomes.

### Example
For login:
- If username valid and password valid → allow login
- If username valid and password invalid → show error
- If username invalid and password valid → show error
- If both invalid → show error

This method is useful for rule-based logic.

---

## 10. State Transition Testing

State transition testing validates behavior when an application moves from one state to another.

### Example
- User logged out → login → logged in → logout → logged out

This is useful in workflows like login, shopping cart, or approval systems.

---

## 11. Defect Life Cycle
- **Defect**: If a feature or functionality is not working according to customer requirements, it is called a defect.

1. Defect
   1. Severity
      - Blocker
      - Critical
      - Major
      - Minor

   2. Priority
      - High
      - Medium
      - Low

### Severity
Severity describes the impact of the defect on the system.

Examples:
- Critical: application crashes, data loss, or security issue
- Major: important feature is broken
- Moderate: feature works but in a limited way
- Minor: cosmetic or minor usability issue

### Priority
Priority defines how quickly the defect needs to be fixed.

Examples:
- P1: fix immediately
- P2: fix in next release
- P3: fix when time allows

> Severity is about business/system impact; priority is about urgency.

### A Defect Goes Through Several Stages
1. New
2. Assigned
3. Open
4. In Progress
5. Fixed
6. Retest
7. Verified
8. Closed
9. Reopened (if required)

### Diagram

```mermaid
flowchart LR
    A[New] --> B[Assigned]
    B --> C[Open]
    C --> D[In Progress]
    D --> E[Fixed]
    E --> F[Retest]
    F --> G[Verified]
    G --> H[Closed]
    G --> I[Reopened]
```

---

### Bug Report Template
A proper defect report usually includes:
- Defect ID
- Title
- Severity
- Priority
- Module/Feature
- Environment
- Steps to reproduce
- Expected result
- Actual result
- Screenshots/video
- Assignee
- Status

### Duplicate Defects
When the same defect is reported multiple times, it is considered a duplicate. The tester should avoid duplicate entries and use the existing defect ID.

---

### Defect Rejection
A defect can be rejected if it is not reproducible, not valid, or outside the product requirements.

### Common Rejection Reasons
- Not reproducible
- Duplicate
- Not a valid defect
- Requirement mismatch due to misunderstanding

---

### Defect Closure
A defect is closed when:
- The fix is implemented
- Retest passes
- The developer and tester agree the issue is resolved

---

## 12. ISTQB Questions

### 1. What is a Defect?
If a feature or functionality is not working according to customer requirement, it is called a **defect**.

**OR**

Deviation from the customer requirement specification is called a **defect**.

### 2. Because of What Defect/Mistake Done by Developer Will There Be a Defect in Software?
- Wrong implementation
- Extra implementation
- Missing implementation

### 3. What Is the Difference Between Error, Bug, Failure, and Defect?
- **Error**: A mistake in the code that prevents compilation or execution is called an **error**.
  - Mainly used by **developers**.
- **Defect**: An error found in the software is called a **defect**.
- **Bug**: Bug is an informal name for a defect and is also a defect accepted by developers.
- **Failure**: Many defects present in the software can lead to **failure**.
  - Mainly used by **end users/customers**.

### 4. Why Do We Do Testing?
- To ensure quality
- To ensure all requirements are implemented correctly

### 5. What Are the Types of Defects?
- Wrong implementation
- Functionality defect
- GUI (Graphical User Interface) defect
- Missing implementation
- Performance defect
- Database defect
- Blocker defect
- Web security defect
- Critical defect
- Major defect
- Minor defect

### 6. Yellow Box Testing
Testing the **warning messages** of an application is called **Yellow Box Testing**.

It is a subset of **Usability Testing**.

**Examples:**
- Battery full
- Battery about to die
- Storage full

### 7. Formal Testing
Testing the software by following procedures, guidelines, or documents is called **Formal Testing**.

Here, we document all:
- Test plans
- Test cases
- Test scenarios

We also review all documents.

### 8. Informal Testing
Testing the software without following procedures, guidelines, or documents is called **Informal Testing**.

Here, we do not have documented:
- Test plans
- Test cases
- Test scenarios

### 9. Accessibility Testing / ADA Testing
**ADA = American Disability Act**

Testing the application/software from the point of view of physically challenged people is called **Accessibility Testing**.

**Example:** ATM testing for deaf and dumb people.

### 10. Fatal Defect / Blocker / Show Stopper
It is another name given to a **Blocker Defect**.

Because of this defect, the test engineer will be completely blocked from testing the assigned module.

It is called:
- Blocker defect
- Show stopper
- Fatal defect

**Example:**
`YouTube [Home] → [404 Error / Blank Page] → Blocker Defect`

### 11. Deferred Defect / Minor Defect / Trivial Defect
It is another name given to a **minor defect** which will not affect the customer's business workflow.

This type of defect is called:
- Minor defect
- Deferred defect
- Trivial defect

### 12. Defect Release / Bug Release
Releasing the software with a known set of defects is called **Bug Release** or **Defect Release**.

These known defects are generally minor and within an acceptable limit.

### 13. Defect Leakage / Bug Leakage
A defect missed by a test engineer but caught by the customer is called **Defect Leakage** or **Bug Leakage**.

### 14. Defect Seeding
The process of intentionally inserting defects into software by the developer is called **Defect Seeding**.

### 15. What Are the Types of Software Testing?
There are multiple ways to classify software testing.

**1st Answer:**
- WBT (White Box Testing)
- BBT (Black Box Testing)
- Grey Box Testing

**2nd Answer:**
- Functional Testing
- Non-Functional Testing

**3rd Answer:**
- Static Testing
- Dynamic Testing

**4th Answer:**
- QA (Quality Assurance)
- QC (Quality Control)

### 16. Functional Testing vs Non-Functional Testing

| Functional Testing | Non-Functional Testing |
| --- | --- |
| Functional Testing | Usability Testing |
| Integration Testing | Performance Testing |
| System Testing | Recovery Testing |
| Smoke Testing | Reliability Testing |
| Regression Testing | GUI Testing |
| Adhoc Testing | Yellow Box Testing |
| Exploratory Testing | Globalization Testing |
| Alpha & Beta Testing | Comparison Testing |
| Acceptance Testing | Compatibility Testing |
|  | Migration Testing |
|  | Web Security Testing |

### 17. Static Testing vs Dynamic Testing

| Static Testing | Dynamic Testing |
| --- | --- |
| Static testing involves all verification activities. | Dynamic testing involves all validation activities. |
| Verification activities include reviews, walkthroughs, inspection, and auditing. | Validation includes actual testing such as FT, IT, ST, Smoke, Adhoc Testing, etc. |
| Here we try to prevent defects. | Here we try to find defects. |
| Static testing is done before the software is developed. | Dynamic testing is done after the software is developed. |
| In static testing we ensure we are building the product right. | In dynamic testing we ensure we are building the right product. |
| It is less costly. | It is more costly. |
| Here we do not execute the code. | Here we execute the code. |

### 18. QA (Quality Assurance) vs QC (Quality Control)

| QA (Process) | QC (Product) |
| --- | --- |
| 1. QA is the set of activities that ensures quality in the process. | 1. QC is the set of activities that ensures quality in the product. |
| 2. This is proactive. | 2. This is reactive. |
| 3. Aims to prevent defects. | 3. Aims to find defects. |
| 4. Verification is the best example for QA. | 4. Validation is the best example for QC. |
| 5. QA is process-oriented. | 5. QC is product-oriented. |
| 6. The goal of QA is to improve development and testing processes so defects do not arise in the future. | 6. The goal of QC is to find defects in the software during testing. |
| 7. QA is planning. | 7. QC is executing the plan. |
| 8. We identify weaknesses in the process and try to improve them. | 8. We try to identify defects in the software and improve product quality. |

### 19. Performance Testing / Baseline Testing / Breakpoint Testing / Benchmark Testing / Spike Testing / Bottleneck Testing / Threshold Testing
Testing the **stability and response time** of an application by applying load is called **Performance Testing**.

The requirement specifying performance testing is called the **Baseline Document**.

Performance testing is also referred to as **Baseline Testing, Breakpoint Testing, Benchmark Testing, Spike Testing, Bottleneck Testing,** or **Threshold Testing** in different contexts.

- **Load**: Load is nothing but the designed number of users.
  - Load can be specified by the customer, BA, senior developer, senior test engineer, or manager.

**Example: Facebook**
`Login → Load ← 10,000 users try to login at the same time → Home`

### 20. Stability and Response Time
**Stability**: The ability of an application to withstand the designed load (number of users) is called the stability of the application.

**Response Time**: Response time is the total time taken to:
- Send the request from the browser to the server (`T1`)
- Run the program on the server (`T2`)
- Get the response from the server back to the browser (`T3`)

**Example:**
If the home page is displayed successfully for all 10,000 users, it is called the **stability of the application**.

If the customer requirement says the home page should be displayed for all 10,000 users within 10 seconds, then **10 seconds is the response time**.

### 21. Types of Performance Testing
There are five types:
- Load Testing
- Stress Testing
- Volume Testing
- Scalability Testing
- Soak / Endurance Testing

**Example Performance Requirement:**
- Load: 10,000 users
- Response Time: 10 seconds

`Amazon.com Login → Home`

#### 1. Load Testing (`<=`)
Testing the stability/response time of an application by applying a load that is **less than or equal to the designed number of users** is called **Load Testing**.

| Load | Response Time | Result |
| ---: | ---: | --- |
| 6,000 | 6 sec | Displayed |
| 10,000 | 10 sec | Displayed |
| 1,000 | 11 sec | Displayed, but load testing fails because response time exceeds the requirement |

#### 2. Stress Testing
Testing the stability/response time of an application by applying a load that is **greater than the designed number of users** is called **Stress Testing**.

| Load (>) | Response Time | Result |
| ---: | ---: | --- |
| 11,000 | 7 sec | Displayed |
| 12,000 | 7 sec | Displayed |
| 15,000 | 8 sec | Displayed |
| 20,000 | 9 sec | Not displayed |

#### 3. Volume Testing
Testing the stability/response time of an application by transferring a **huge amount/volume of data** is called **Volume Testing**.

It is mainly done to check the **capacity of the database server**.

**Example:**
`System → Server → Database → Huge amount / volume of data in the database`

#### 4. Scalability Testing
Testing the stability and response time of an application by applying a load greater than the designed number of users and checking the **break point** of the application (the point where the application/software crashes) is called **Scalability Testing**.

| Load | Response Time | Result |
| ---: | ---: | --- |
| 25,000 | 7 sec | Displayed |
| 35,000 | 8 sec | Displayed |
| 40,000 | 8 sec | Displayed |
| 45,000 | 12 sec | Not displayed |

#### 5. Soak Testing / Endurance Testing
Testing the stability and response time of an application by applying load **continuously for a particular period of time** is called **Soak Testing / Endurance Testing**.

**Example:**
Suppose you logged in to a Yahoo application and used it without logging out for two days. When you try to use/launch the application again, it should still work properly.

### 22. How to Do Performance Testing Manually
**Customer Requirement:**
- Load: 10 users
- Response Time: 10 seconds

`10 users → Test Engineer → Server → Performance Testing Manually`

- Start Time = `--:--`
- Stop Time = `--:--`

If the customer gives a very high load, such as **1 crore users**, we cannot do it manually because the number of users is too high. This is one reason we use **automation tools**.

**Performance Testing Tools Available in the Market:**
- LoadRunner — Licensed version
- JMeter
- NeoLoad
- QA Load
- Silk Performance Tool
- Rational Performance Tool

### 23. How Does the Performance Testing Tool Look / Work?

#### LoadRunner
**Buttons:**
- Start Recording
- Stop Recording
- Play (`>`)
- Pause (`||`)
- Stop

**Inputs:**
- Enter the URL
- Number of users
- Start time
- Stop time
- Date & Time

**Steps:**
1. Click the **Start Recording** button.
2. Perform the action, such as opening the browser and entering the URL.
3. Click the **Stop Recording** button.
4. The performance testing tool converts the performed actions into an automation script.

### Continuation of LoadRunner Process
- Enter the URL and number of users into the tool.
- Click the **Play / Run** button.
- VUGen generates the required number of dummy users.
- Click the **Stop** button when the test is completed.
- Record the start time and end time in the tool.
- All users from their respective browsers send requests to the server (`T1`).
- The program runs on the server (`T2`).
- The server sends the response back to all users (`T3`).

**Note:** In some performance tools, system time is taken by default.

### 24. Thick Client / Standalone Application / Client-Server Application
A software application installed on the **client machine** is called a **Thick Client**.

**Examples:**
- Microsoft Word
- Notepad
- WhatsApp
- Chrome Browser
- Facebook APK

### 25. Thin Client / Web Application
A software application where the software is installed on the **server** and users access it to perform work is called a **Thin Client**.

**Examples:**
- Gmail — [www.gmail.com](https://www.gmail.com)
- Facebook — [www.facebook.com](https://www.facebook.com)

### 26. Testware
**Testware** is terminology used to describe the documents/artifacts used while testing software.

**Examples:**
- Test Scenarios
- Test Cases
- Defect Reports
- Traceability Matrix
- Test Scripts
- Test Plan

### 27. Interrupt Testing
It is the process of replicating an **interrupt** or an abrupt interruption in an application/software to verify how the application behaves.

### 28. Types of Requirement
- Functional Requirement
- Non-Functional Requirement

**Functional Requirements are tested using:**
- Functional Testing
- Integration Testing
- System Testing
- Smoke Testing
- Acceptance Testing
- Adhoc Testing
- Regression Testing

**Non-Functional Requirements are tested using:**
- Performance Testing
- Usability Testing
- Globalization Testing
- Compatibility Testing
- Migration Testing
- Comparison Testing

### 29. Migration Testing
Whenever the technology is outdated or the database is outdated, we migrate from the old technology/database to a new/latest technology/database.

Testing during this migration is called **Migration Testing**.

**Example:**
`Old Technology (1997: Mainframe, SQL) → New Technology (2022: Java, Oracle)`

### 30. Comparison Testing / Parallel Testing
Here we compare a newly built application with a similar application released in the market.

We check:
- Strengths and weaknesses
- Advantages and disadvantages
- Whether all required features are present in our newly built application

This is called **Comparison Testing**.

**Examples:**
- Flipkart → Amazon
- Telegram → WhatsApp
- Zomato → Swiggy
- UpGrad → Unacademy
- Ola → Uber

### 31. Failure
Deviation from the requirement specification that is **visible to the end user** is called **Failure**.

### 32. How to Calculate Defect Density?
**Defect Density** is generally calculated as:
`Defect Density = Number of Defects / Size of the Software`

**Example:**
If a module has 20 defects and the module size is 10 KLOC:
`Defect Density = 20 / 10 = 2 defects per KLOC`

### 33. When to Do Testing?
Testing can be performed based on the project situation, for example:
- When the product is functionally stable (good quality)
- When the basic functionality itself is not working (blocker)
- When the time span is less, test all basic and important features and then stop testing
- When there is no budget

### 34. Defect Masking / Fault Masking / Bug Masking / Defect Hiding
One defect hiding another defect is called **Defect Masking**.

**Example: Instagram**
- **Build B1:** `Home → [Blank Page] → Defect`
- **Build B2:** `Login → [Blank Page]`

The defect in one area may hide another defect.

### 35. Defect Cascading / Bug Cascading
One defect triggering another defect is called **Defect Cascading**.

**OR**
Defect cascading means one defect causing another defect is called **Defect Cascading**.

**Example: Citibank Application**
`Customer Requirement → Developer writes code + WBT → Home`

Features:
- Amount Transfer
- Amount Balance
- Loan
- Insurance

**Defect:** Amount 500 is debited.

**Amount Transfer:**
`From [ ] → To [ ] → Amount [-100] → [Transfer] [Cancel]`

**Requirement:** It should accept only positive (`+`) integers.

A confirmation message is displayed.

### 36. Defect Clustering
Some modules consist of most of the defects, and defects are not equally distributed among all modules.

These defects may lead to operational failure, and this concept is called **Defect Clustering**.

**Example:**
- Module A, B → 7 defects
- Module C, D → 6 defects
- 48 defects → Operational failure

> As soon as the Test Engineer gets a build, they should perform smoke testing properly, identify the impacted areas, and perform proper regression testing.

### 37. Principles of Software Testing / Manual Testing
- We should not do exhaustive testing.
- We should do early testing.
- Testing should be done to show the presence of defects in the software.
- We should focus on the **Pesticide Paradox**.
- We should focus on **Defect Clustering**.
- Testing is context-dependent. Depending on the type of application and how the customer will use it, testing should be planned accordingly.
- Absence of errors in the application does not mean the application is free from defects.

### 38. Pesticide Paradox
If you run the same test cases for many executions, those test cases may lose their capability to catch new and creative defects. This concept is called the **Pesticide Paradox**.

To overcome this, we should keep updating and improving the test cases from time to time.

**Example:**
`Release 1 → Module A → 100 Test Cases → Update for every release`

### 39. What Is a Latent Defect?
A defect that is present in the software but is not identified for a particular period of time is called a **Latent Defect**.

### 40. What Is a Use Case?
A **Use Case** is a pictorial representation of a requirement that explains how the end user interacts with the application and describes the possible ways the end user can use the application.

**Example: QSpiders**

**Features:**
- Attendance
- Mock Rating
- Fees Details
- Date of Joining
- Masterly
- Education

**Roles:**
- HR
- Counselor
- Trainer
- Students
- Attendance Team
- Admin

### 41. What Are the Levels of Testing?
- Unit Testing
- Integration Testing
- System Testing
- Acceptance Testing

### 42. Test Basis
**Test Basis** is a document/source used to write test cases.

**Examples:**
- CRS
- BRS
- Use Case
- FS

### 43. Test Artifacts
These are the set of documents used by the Test Engineer during the **STLC process**:
- Test Strategy
- Test Plan
- Test Scenarios
- Test Cases
- Traceability Matrix
- Test Execution Reports
- Defect Report Template

### 44. Compliance Testing
It is a type of **non-functional testing** performed to check whether the software developed meets the company's standards or the respective organizational standards.

### 45. Pilot Testing
Pilot Testing is done by a selected set of people who perform a trial run on the project and provide feedback to the company before releasing the software to customers.

### 46. Risk-Based Testing
Risk-Based Testing is testing performed by the Test Engineer based on **risk**.

Here, the Test Engineer prioritizes and tests the features/functionality of the application that have a **high risk of failure**.

### 47. Reliability Testing
Testing the functionality of an application continuously for a particular period of time is called **Reliability Testing**.

- It is mainly done for **Standalone** and **Client-Server applications**.
- Doing Reliability Testing manually is very tough, so we can use automation tools to perform it.

### 48. Difference Between Reliability Testing and Soak Testing

| Reliability Testing | Soak / Endurance Testing |
| --- | --- |
| Testing the functionality of an application continuously for a particular period of time is called Reliability Testing. | Testing the stability and response time of an application by applying load continuously for a particular period of time is called Soak / Endurance Testing. |
| It is mainly done for Standalone and Client-Server applications. | It is mainly done for Web Applications and Client-Server applications. |
| Here we do not apply load. | Here we apply load. |

### 49. Recovery Testing
Testing the functionality of the application to check how well it recovers from **crashes or disasters** is called **Recovery Testing**.

- Recovery Testing is mainly done for **Standalone** and **Client-Server applications**.

**Example:**
`WhatsApp → [Chats | Status | Call] → "WhatsApp isn't responding"`

### 50. Difference Between Prototype and Use Case

| Prototype | Use Case |
| --- | --- |
| Prototype module is a dummy module created by developers where text is converted into image format. | Use Case is a pictorial representation of a requirement and explains how the end user interacts with the application. |

### 51. Smoke Testing vs Sanity Testing

| Smoke Testing | Sanity Testing |
| --- | --- |
| Smoke testing is shallow and wide testing. | Sanity testing is narrow and deep testing. |
| Shallow = high level; wide = covers all basic and critical features. | Here, one component is selected and tested deeply. |
| **Example:** `[Compose: To, CC, Subject]` → Test only the basic and critical areas of all features, mainly positive scenarios. | **Example:** `[Compose: To, CC, Subject]` → Select one component and test all positive and negative scenarios. |
| Smoke testing is generally positive testing. | Sanity testing includes both positive and negative testing. |
| Smoke test cases and scenarios are documented. | Test cases/scenarios are generally not separately documented. |
| Automation can be used for smoke testing. | Sanity testing is generally performed without dedicated automation. |
| It can be performed by both developers and testers. | It is mainly performed by the Test Engineer. |

### 52. SDLC vs STLC

| SDLC | STLC |
| --- | --- |
| SDLC is a step-by-step or standard procedure to develop new software/application. | STLC is a step-by-step or standard procedure to test a new feature of an application. |
| SDLC stands for **Software Development Life Cycle**. | STLC stands for **Software Testing Life Cycle**. |
| STLC is part of SDLC. | Defect Life Cycle is part of STLC. |

#### SDLC Stages
`Requirement → Feasibility Study (FS) → Design → Coding → Testing → Installation → Maintenance`

#### STLC Stages
`System Study → Write Test Plan → Write Test Case → Traceability Matrix → Execute Test Case → Defect Tracking → Prepare Test Case Execution Report → Postmortem Meeting`

### 53. Difference Between Regression Testing and Re-Testing

| Regression Testing | Re-Testing |
| --- | --- |
| 1. Testing the unchanged/old feature to make sure changes such as adding, removing, modifying, or fixing a defect do not introduce defects in the unchanged/old feature is called **Regression Testing**. | 1. Whenever the Test Engineer gets a new build, checking whether the defect is fixed or not is called **Re-Testing**. |
| 2. Regression testing is done for passed test cases. | 2. Re-testing is done for failed test cases. |
| 3. Regression testing is generic testing. | 3. Re-testing is planned testing. |
| 4. We can use automation for regression testing. | 4. We generally do not automate re-testing separately. |
| 5. Regression testing generally takes less priority compared to re-testing. | 5. Re-testing generally takes higher priority compared to regression testing. |

**Question:** Is there any difference between Unit Regression Testing and Re-Testing?

**Answer:** Yes.

**Example:**
`SBI → Amount Transfer → Requirement: It should accept ...`