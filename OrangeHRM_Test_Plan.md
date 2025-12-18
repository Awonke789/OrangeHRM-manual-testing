# OrangeHRM Test Plan

**Software Testing**
Awonke Lubelwana (Group Leader), Alulutho Tokwe, Buhle Palaza, Caleigh Goliath, Iviwe Hlatana
CAPACITI 17 October 2025

## Table Of Contents
1.0 Introduction
1.1 Objective
1.2 Project Description
1.3 Process Tailoring & Test Types
2.0 Assumptions/Dependencies
3.0 Test Requirements
9.0 Entry Criteria
10.0 Exit Criteria
11.0 Screenshots For Evidence

## 1.0 Introduction
This document outlines the test plan for evaluating the functionality and user experience of the OrangeHRM Web Application, an open-source Human Resource Management platform. The primary goal is to ensure that the application meets its intended requirements and provides stable, reliable experience for end-users. This plan defines strategy, scope, resources, and schedule for testing, ensuring all core functionalities are tested thoroughly using both manual and automated approaches.

### 1.1 Objective
The main goal of this testing effort is to:
*   Verify the core functionalities of the OrangeHRM Demo application against system requirements.
*   Find defects and deviations from expected behavior.
*   Ensure a smooth and intuitive user experience across key user flows.
*   Validate the stability and reliability of the application under various scenarios.
*   Provide guidance for the planning, design, execution, and reporting of all test activities in alignment with the system requirements.

### 1.2 Project Description
OrangeHRM is a comprehensive HR management platform offering modules such as employee information management, leave management, time tracking, and recruitment. The purpose of this project is to perform end-to-end functional and automation testing on its demo environment, available at https://opensource-demo.orangehrmlive.com/.

This testing project follows a hybrid Agile–Waterfall model, focusing on early test design, followed by manual testing, bug reporting, and automation.

### 1.3 Process Tailoring & Test Types
Testing types planned include:
*   **Functional Testing:** To verify that each feature and function of the application is used in compliance with the requirements.
*   **Regression Testing:** To ensure that latest changes or fixes have not adversely affected existing functionalities.
*   **UI/UX Testing:** To verify the graphical user interface elements and overall layout for consistency and usability and validate responsiveness.
*   **Automation Testing:** Automate core test flows using Selenium WebDriver.
*   **Performance Testing (optional):** For response validation under load.

## 2.0 Assumptions/Dependencies

### Assumptions:
*   The OrangeHRM demo environment will be available and stable during testing.
*   Testers will have valid credentials to access all modules.
*   The testing environment will mirror production settings for consistency.
*   Test data (employee records, leave details) will be created and maintained by the QA team.

### Dependencies:
*   Availability of a stable OrangeHRM Demo application environment.
*   Access to valid test credentials.
*   Completion of test plan and test case documentation.
*   Application accessibility and up time of the demo environment.
*   Completion of any system maintenance before the start of testing.
*   Browser drivers and Selenium setup configured prior to automation testing.

## 3.0 Test Requirements
Testing will be performed against the following system requirements extracted from the application features:

| ID | Requirement Description | Test Case ID(s) |
| :--- | :--- | :--- |
| R1 | Verify user login and logout functionality. | TC\_OHRM\_001, TC\_OHRM\_002, TC\_OHRM\_006 |
| R2 | Validate the Dashboard page loads with widgets and menus. | (To be added) |
| R3 | Ensure new employees can be added successfully in the PIM module. | TC\_OHRM\_003 |
| R4 | Validate employee search, edit, and delete operations. | (To be added) |
| R5 | Test leave application submission and approval workflow. | TC\_OHRM\_004 |
| R6 | Verify recruitment process ‒ posting vacancies and adding candidates. | (To be added) |
| R7 | Ensure role-based access control for Admin vs. Employee users. | (To be added) |
| R8 | Validate input form field validations and error messages. | (To be added) |
| R9 | Confirm responsiveness and navigation across browsers. | (To be added) |
| R10 | Automate key functional flows (login, add employee, leave request). | (To be added) |
| R\_Buzz\_001 | User can access the Buzz section and interact with posts. | TC\_OHRM\_007 |
| R\_MyInfo\_001 | User can view their personal information under 'My Info'. | TC\_OHRM\_005 |

## 4.0 Test Tools

| Tool | Purpose |
| :--- | :--- |
| Excel | Manual test case documentation, Test Case Management |
| Selenium WebDriver | Automation testing |
| JUnit | Test execution and result validation |
| GitHub Issues | Bug tracking and management |
| Snipping Tool | Capturing evidence and screenshots |
| Browsers: Chrome, Edge, Firefox | Cross-browser validation |
| Text Editor | For documenting test plans and cases |

## 5.0 Resource Requirements

| Resource Type | Description | Quantity |
| :--- | :--- | :--- |
| Test Engineer | Responsible for creating and executing test cases | 1 |
| QA Lead | Oversees planning, reviews reports | 1 |
| Automation Engineer | Develops Selenium scripts | 1 |
| Test Environment | OrangeHRM Demo Site (Web-based) | 1 |
| Hardware | Laptop/PC with 8GB RAM, Chrome browser | 1–2 |
| Operating System | Ubuntu 22.04 (Sandbox Environment) | N/A |
| Test Data | Provided credentials for OrangeHRM (Admin/admin123) | N/A |

## 6.0 Test Schedule

| Phase | Task | Duration | Timeline |
| :--- | :--- | :--- | :--- |
| Week 1 | Test Planning & Test Design | 1 week | 2025-10-17 to 2025-10-18 |
| Week 2 | Manual Execution & Bug Reporting | 1 week | 2025-10-21 to 2025-10-23 |
| Week 3 | Selenium Automation Setup & Scripting | 1 week | (To be determined) |
| Week 4 | Reporting & Final Review | 1 week | 2025-10-26 to 2025-10-27 |

## 7.0 Risks/Mitigation

| Risk | Impact | Mitigation |
| :--- | :--- | :--- |
| Demo site downtime | High | Use cached test data; re-run tests after uptime |
| Selenium driver incompatibility | Medium | Update drivers and maintain version control |
| Browser updates breaking scripts | Medium | Regular regression runs after browser updates |
| Data loss between sessions | Low | Maintain manual backups of test data |
| Limited time for automation | Medium | Prioritize high-value test cases for automation |

## 8.0 Metrics
The following metrics will be collected during and after the test cycles:

### Prior to Delivery:
*   Number of planned vs executed test cases
*   Defects identified per module and severity
*   Test pass/fail percentage
*   Effort (in hours) spent on manual vs automation testing
*   Test execution progress (percentage complete).
*   Test coverage (percentage of requirements covered by test cases).

### Post Delivery:
*   Number of post-release defects (if any)
*   Time to execute full regression suite
*   Automation coverage percentage

## 9.0 Entry Criteria
*   Approved Test Plan document.
*   All test cases designed and reviewed.
*   Test environment set up and accessible.
*   Test data prepared and available.
*   Application builds deployed and stable.

## 10.0 Exit Criteria
*   All critical and major defects were resolved and retested.
*   95% of planned test cases were executed.
*   90% of executed test cases passed.
*   Test Summary Report approved.

## 11.0 Screenshots For Evidence
(Screenshots are not included in this text-based file, but the sections are noted)
*   Feature 1: Dashboard
*   Feature 2: Login Page
*   Feature 3: Unsuccessful Login (Invalid Credentials)
*   Feature 4: PIM (Personnel Information Management) Module
*   Feature 5: Leave Landing Page
*   Feature 5.2: Apply Leave in Detail
*   Feature 6: My Info Page
*   Feature 7: Logout Functionality
*   Feature 8: Buzz Feed

## 12.0 Definitions and Acronyms
*   **OrangeHRM:** Human Resource Management system.
*   **PIM:** Personnel Information Management.
*   **UI:** User Interface.
*   **UX:** User Experience.
*   **SRS:** Software Requirements Specification.
*   **QA:** Quality Assurance.
