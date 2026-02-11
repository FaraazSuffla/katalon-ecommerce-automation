# Katalon E-Commerce Automation (Sauce Demo)

[![Katalon Studio](https://img.shields.io/badge/Katalon%20Studio-10.4.3-2C7BE5)](https://katalon.com/)
![Type](https://img.shields.io/badge/Type-WebUI-6C757D)
![Approach](https://img.shields.io/badge/Approach-Record%20%26%20Playback-6C757D)

Web UI automation project built with **Katalon Studio** using **Record & Playback** (no custom code). The focus is a clean, portfolio-friendly example of **real-world QA automation practices**: positive/negative scenarios, stable waits, reusable locators, and clear validations.

**Current repo coverage**: Login automation (positive + negative). Additional e-commerce flows are **planned** but not yet committed as automated tests.

## Table of Contents
- [Application Under Test](#application-under-test)
- [Current Coverage](#current-coverage)
- [Tools & Technologies](#tools--technologies)
- [Quick Start (Katalon Studio)](#quick-start-katalon-studio)
- [Test Credentials (Sauce Demo)](#test-credentials-sauce-demo)
- [Project Structure](#project-structure)
- [Test Cases Included](#test-cases-included)
- [Reports & Artifacts](#reports--artifacts)
- [Roadmap](#roadmap)
- [Notes](#notes)

## Application Under Test
**Sauce Demo**: [https://www.saucedemo.com](https://www.saucedemo.com)

## Current Coverage
### In scope (implemented in this repo)
- Login (positive + negative)

### Planned scope (not yet automated here)
- Product listing
- Add to cart
- Checkout
- Logout

### Out of scope
- Performance testing
- Security testing
- Cross-browser testing

## Tools & Technologies
- **Katalon Studio 10.4.3** (WebUI)
- **Selenium** (bundled with Katalon WebUI)
- **Object Repository** for centralized locator management

## Quick Start (Katalon Studio)
1. Clone this repository.
2. Open Katalon Studio.
3. Open the project file: `Katalon-ecommerce-automation/Katalon-ecommerce-automation.prj`
4. In the Test Explorer, go to `Test Cases/Login/`.
5. Run a test case via **Run → Chrome**.

## Test Credentials (Sauce Demo)
Use these for the positive login scenario:

```text
username: standard_user
password: secret_sauce
```

## Project Structure
Repository layout (simplified):

```text
.
├─ README.md
└─ Katalon-ecommerce-automation/
   ├─ Katalon-ecommerce-automation.prj
   ├─ Test Cases/
   │  └─ Login/
   ├─ Object Repository/
   │  └─ LoginPage/
   ├─ Profiles/
   ├─ settings/
   └─ console.properties
```

Katalon-specific notes:
- **`Test Cases/`** contains the automated flows (`.tc`).
- **`Object Repository/`** contains saved UI elements/locators (`.rs`).
- **`Profiles/`** holds execution profiles (global variables).
- **`Test Suites/`** are not included yet in this repo (tests are run individually for now).
- **`Keywords/`** / custom Groovy keywords are not used yet (Record & Playback focused).

## Test Cases Included
| Test Case | Description | Tags |
|-----------|-------------|------|
| `TC_Valid_Login_RnP` | Valid login for `standard_user`; verifies Products page is displayed | Login, Positive, Smoke |
| `TC_Invalid_Password_RnP` | Login with invalid password; verifies error message | Login, Negative, Regression |
| `TC_Empty_Credentials_RnP` | Login with empty username/password; verifies validation message | Login, Negative, Regression |

## Reports & Artifacts
Katalon generates execution artifacts after a run (commonly under a `Reports/` folder inside the Katalon project directory).  
If you want reports committed later, consider adding a `.gitignore` rule and/or exporting HTML/PDF summaries.

## Roadmap
- Add test cases for product listing, add-to-cart, checkout, and logout
- Add a `Test Suites/` collection for a one-click smoke/regression run

## Notes
- Element maintenance is centralized in the **Object Repository** (CSS/XPath selectors).
- If a test is flaky due to timing, prefer using Katalon’s built-in waits (e.g. `waitForElementVisible`, `waitForElementClickable`) rather than hard sleeps.
