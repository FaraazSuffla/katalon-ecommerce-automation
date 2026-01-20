# Katalon E-Commerce Automation

## Project Overview
Web UI automation project built using **Katalon Studio Record & Playback**, without writing any code.  
The goal of this project is to demonstrate **real-world QA automation practices**, including test design, positive and negative testing, and maintainable test structure.

---

## Application Under Test
**Sauce Demo**  
[https://www.saucedemo.com](https://www.saucedemo.com)

---

## Test Scope

### In Scope
- Login functionality (positive and negative scenarios)  
- Product listing  
- Add to cart  
- Checkout process  
- Logout  

### Out of Scope
- Performance testing  
- Security testing  
- Cross-browser testing  

---

## Tools & Technologies
- Katalon Studio (Record & Playback)  
- Selenium (built-in with Katalon)  
- GitHub Desktop for version control  

---

## Test Design Approach
- Manual test cases designed before automation  
- Positive and negative scenarios recorded with Katalon Recorder  
- Object Repository used for element management  
- Assertions added for validation (via Record & Playback)  
- Waits (`waitForElementVisible`, `waitForElementClickable`) added for stable execution  
- Descriptions and tags added for clarity and portfolio-readiness  

---

## How to Run the Tests
1. Clone this repository  
2. Open the project in **Katalon Studio**  
3. Open the **Test Cases** or **Test Suites** folder  
4. Select the desired test case or test suite  
5. Click **Run → Chrome**  

---

## Test Cases Included
| Test Case | Description | Tags |
|-----------|-------------|------|
| `TC_Valid_Login_RnP` | Valid login for `standard_user`; verifies Products page is displayed | Login, Positive, Smoke |
| `TC_Invalid_Password_RnP` | Login with invalid password; verifies error message | Login, Negative, Regression |
| `TC_Empty_Credentials_RnP` | Login with empty username/password; verifies validation message | Login, Negative, Regression |
