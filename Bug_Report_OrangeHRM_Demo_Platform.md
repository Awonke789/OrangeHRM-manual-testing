# Bug Report - OrangeHRM Demo Platform

**Authors:** Alulutho Tokwe, Awonke Lubelwana, Buhle Palaza, Caleigh Goliath, Iviwe Hlatana
**Date:** 24 October 2025
**Organization:** Capaciti

## Overview
This document outlines the bugs identified during the execution of Week 1 and Week 2 test cases, including newly discovered defects and UI usability issues observed on the OrangeHRM Demo Platform (https://opensource-demo.orangehrmlive.com/).

---

## Bugs Logged

### Bug ID: BUG-OHRM-001
*   **Title:** Apply Leave Functionality Displays "No Leave Types with Leave Balance".
*   **Module:** Leave/Apply
*   **Severity:** High
*   **Priority:** High
*   **Description:** When a user tries to apply for leave through the 'Leave' module, the system displays a message stating "No Leave Types with Leave Balance." This prevents the user from going ahead with any leave application.
*   **Steps to Reproduce:**
    1.  Log in to the OrangeHRM demo platform as an Admin.
    2.  Navigate to the 'Leave' section from the left-hand menu.
    3.  Click on the 'Apply' sub-menu.
    4.  Observe the message "No Leave Types with Leave Balance" displayed on the page.
*   **Expected Result:** The system should present a form or an interface allowing the user to select leave types, specify dates, and submit a leave application, assuming leave types and balances are configured.
*   **Actual Result:** The system displays "No Leave Types with Leave Balance," blocking the leave application process.

---

### Bug ID: BUG-OHRM-002
*   **Title:** "Forgot your password?" Link Missing from Login Page or Rest password page, and forgot Password Functionality Reveals User Existence Through Identical Success Messages
*   **Module:** Authentication / Password Reset
*   **Severity:** High
*   **Priority:** High
*   **Description:** The login page of the OrangeHRM demo has a “Forgot password “button or link, but it does not function as expected, which is a standard feature for user convenience and account recovery. Additionally, the "Forgot Password" feature displays identical success messages for both valid and invalid usernames, creating a user enumeration vulnerability that allows attackers to determine valid system usernames.
*   **Steps to Reproduce:**
    1.  Navigate to the OrangeHRM login page (https://opensource-demo.orangehrmlive.com/).
    2.  Observe the elements present on the login page.
    3.  Click the “Forgot password” button.
    4.  Enter Username and click “Reset Password”.
    *Second Steps to Reproduce:*
    1.  Navigate to OrangeHRM login page
    2.  Click "Forgot your password?" link
    3.  Enter an invalid username (e.g., "nonexistentuser123")
    4.  Click "Reset Password" button
    5.  Observe the success message
*   **Expected Result:** A "Forgot your password?" link should be sent to the user or Admin. For invalid usernames, the system should show generic messaging that doesn't confirm or deny username existence.
*   **Actual Result:** No "Forgot your password?" link is sent to the Admin or User, and the System displays an identical success message for ALL usernames (valid and invalid): "Reset Password link sent successfully. A reset password link has been sent to you via email."

---

### Bug ID: BUG-OHRM-003
*   **Title:** Application Unexpectedly Switches Languages Spontaneously
*   **Module:** Internationalization/Localization
*   **Severity:** Medium
*   **Priority:** Medium
*   **Description:** The application unexpectedly switched the entire user interface from English to Chinese without any user-initiated language change action. The issue resolved itself after several page reloads.
*   **Steps to Reproduce:**
    1.  Navigate to OrangeHRM login page (initially in English)
    2.  Observe spontaneous language change to Chinese
    3.  Login to application
    4.  Observe entire application remains in Chinese language
    5.  Reload page multiple times to see language switch back to English
*   **Expected Result:** Application should maintain consistent language (English by default) unless explicitly changed by the user.
*   **Actual Result:**
    1.  Application spontaneously switched to Chinese language
    2.  All UI elements displayed in Chinese
    3.  Language change persisted across pages
    4.  Language switched back to English after several pages reload

---

### Bug ID: BUG-OHRM-004
*   **Title:** Profile Picture Randomly Changes Between Logins
*   **Module:** User Interface
*   **Severity:** Low-Medium
*   **Priority:** Medium
*   **Description:** The application's user profile pictures change randomly between different login sessions without any user configuration changes. This indicates inconsistent user preference storage.
*   **Steps to Reproduce:**
    1.  Logout of OrangeHRM application
    2.  Login again with same credentials
    3.  Observe changes in profile picture
    4.  Repeat logout/login to see additional random changes
*   **Expected Result:** User profile picture should remain consistent across login sessions unless explicitly changed by the user through settings/preferences.
*   **Actual Result:**
    1.  User profile picture changes to different images
    2.  Changes occur without any user action or configuration
    3.  No apparent pattern or user control over the changes

---

### Bug ID: BUG-OHRM-005
*   **Title:** Location dropdown in Job Details has no selectable options, breaking multi-location functionality
*   **Module:** PIM > Employee Job Details
*   **Severity:** Medium
*   **Priority:** Medium
*   **Description:** The Location dropdown field in the Employee Job Details section shows only "- Select -" with no actual location options available. This prevents proper assignment of employees to physical locations, breaking essential HR functionality for multi-location organizations.
*   **Steps to Reproduce:**
    1.  Navigate to PIM > Employee List
    2.  Edit any employee's job details
    3.  Scroll to Location dropdown
    4.  Observe only "- Select -" option is available
    5.  Attempt to select a location - no options appear
*   **Expected Results:** Dropdown should contain multiple location options (e.g., Headquarters, Branch Offices, Remote) or allow admin configuration of locations.
*   **Actual Results:** Location dropdown is essentially non-functional with no selectable options.

---

### Bug ID: BUG-OHRM-006
*   **Title:** Inconsistent background colour.
*   **Module:** User Interface / Login Page
*   **Severity:** High
*   **Priority:** High
*   **Description:** The background color of the OrangeHRM login page changes inconsistently between orange and purple on different page loads or sessions, without any clear reason or theme setting. This creates a confusing and inconsistent user experience.
*   **Steps to Reproduce:**
    1.  Open the OrangeHRM demo site
    2.  Observe the background color of the login page (it may appear orange).
    3.  Refresh the page several times or open it in a new tab.
    4.  Notice that sometimes the background changes to purple instead of orange.
*   **Expected Results:** The background color of the page should remain consistent to maintain the company’s brand image and visual identity.
*   **Actual Results:** The background color of the website/application changes inconsistently over time (e.g., from brown to various other colors), whereas it is expected to remain a consistent orange as per the design specification (Orange).

---

### Bug ID: BUG-OHRM-007
*   **Title:** Username Field is Case Insensitive - Security Concern
*   **Module:** Authentication
*   **Severity:** Medium
*   **Priority:** Medium
*   **Description:** The login system accepts both "Admin" (correct) and "admin" (all lowercase) as valid usernames when paired with the correct password "admin123". This case insensitivity reduces security by allowing multiple username variations.
*   **Steps to Reproduce:**
    1.  Navigate to OrangeHRM login page
    2.  Enter "admin" (all lowercase) in username field
    3.  Enter "admin123" in password field
    4.  Click the "Login" button
*   **Expected Result:** Login should fail or maintain case sensitivity like most secure authentication systems.
*   **Actual Result:** Login succeeds and user is redirected to dashboard. The system treats "Admin" and "admin" as identical usernames.
*   **Attack Surface:** Increases potential for credential stuffing.
