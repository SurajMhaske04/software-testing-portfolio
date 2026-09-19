# Login Test Cases

## Application
SauceDemo

## Feature
Login

## Testing Type
Manual Functional Testing

## Environment
- Browser: Chrome
- Operating System: Windows
- Test Type: Manual
- Test Data Source: SauceDemo provided test credentials

---

## Test Cases

| Test Case ID | Test Scenario | Test Data | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| TC-LOGIN-001 | Verify login with valid credentials | Username: `standard_user`<br>Password: `secret_sauce` | User should successfully log in and reach the products page. | Products page opened successfully. | PASS |
| TC-LOGIN-002 | Verify login with invalid password | Username: `standard_user`<br>Password: `wrong123` | Login should be rejected and an appropriate error message should be displayed. | `Epic sadface: Username and password do not match any user in this service` | PASS |
| TC-LOGIN-003 | Verify login with invalid username | Username: `wrong_user`<br>Password: `secret_sauce` | Login should be rejected and an appropriate error message should be displayed. | `Epic sadface: Username and password do not match any user in this service` | PASS |
| TC-LOGIN-004 | Verify login with both fields empty | Username: Empty<br>Password: Empty | Username-required validation should be displayed. | `Epic sadface: Username is required` | PASS |
| TC-LOGIN-005 | Verify login with empty username | Username: Empty<br>Password: `secret_sauce` | Username-required validation should be displayed. | `Epic sadface: Username is required` | PASS |
| TC-LOGIN-006 | Verify login with empty password | Username: `standard_user`<br>Password: Empty | Password-required validation should be displayed. | `Epic sadface: Password is required` | PASS |
| TC-LOGIN-007 | Verify login with locked-out user | Username: `locked_out_user`<br>Password: `secret_sauce` | Login should be prevented and an appropriate locked-out message should be displayed. | `Epic sadface: Sorry, this user has been locked out.` | PASS |
| TC-LOGIN-008 | Verify password masking | Password: `secret_sauce` | Entered password should be masked. | Password was displayed as dots/bullets. | PASS |
| TC-LOGIN-009 | Verify Login button functionality | Username: Empty<br>Password: Empty | Clicking Login should trigger the appropriate validation. | `Epic sadface: Username is required` | PASS |

---

## Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 9 |
| Executed | 9 |
| Passed | 9 |
| Failed | 0 |
| Blocked | 0 |

### Pass Rate

**100%**

---

## Observations

- Valid credentials successfully opened the Products page.
- Invalid credentials were rejected with an appropriate error message.
- Required-field validation was displayed when mandatory fields were empty.
- The locked-out test user was prevented from logging in.
- Password input was masked.
- The Login button triggered the expected validation behavior.

## Defects

No defects were identified during the login test execution performed for this project.

> **Note:** Absence of defects in these executed cases does not prove that the application is defect-free. Testing was limited to the documented scope and test cases.
