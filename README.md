
# Hybrid-SeleniumEasy-Test-Automation-Framework By Mateusz Konatkowski

Welcome to my Hybrid-SeleniumEasy-Test-Automation-Framework, tailor-made for testing the SeleniumEasy website. This framework is a robust solution crafted to enhance the efficiency and effectiveness of web application testing on <a href="https://demo.seleniumeasy.com/" rel="nofollow">SeleniumEasy</a>
 
 # ✳️ Key Features
 

#### 🟨 Modular Structure:
The framework follows a modular design, allowing you to organize your test cases efficiently.

#### 🟨 Configuration Management:
Easily configure test environments, browsers, and other settings using external properties files.

#### 🟨 Selenium WebDriver Integration:
The framework seamlessly integrates with Selenium WebDriver for easy web automation.

#### 🟨 TestNG Integration:
Harness the full capabilities of TestNG for test execution, parallelization, and reporting.

#### 🟨 Logging and Reporting:
Detailed logs and comprehensive test reports help you identify issues quickly.

#### 🟨 Page Object Model (POM):
Implement the POM design pattern for cleaner and more maintainable page object classes.

#### 🟨 Data-Driven Testing:
Execute tests with various excel test data sets to maximize test coverage.

#### 🟨 Continuous Integration:
Seamlessly integrate your tests with popular Github Actions for automated testing.

#### 🟨 Extensibility:
Extend the framework with custom utilities, listeners, and more to suit  your specific needs.


 ## ✳️ SYSTEM REQUIREMENTS

#### - Install JDK 

#### - Install Chrome Browser, Edge Browser, Firefox Browser

#### - Install Maven

#### - Run well on the Windows platform

#### - Use IntelliJ IDEA is the best choice

## ✳️ Languages and Frameworks

🟨 [Java 17](https://docs.oracle.com/en/java/javase/17/)

🟨 [Selenium 4](https://www.selenium.dev/documentation/)

🟨 [TestNG](https://testng.org/doc/documentation-main.html) 

🟨 [WebDriverManager 5](https://bonigarcia.dev/webdrivermanager/)

🟨 [Maven](https://maven.apache.org/guides/index.html)

🟨 [Log4j2](https://logging.apache.org/log4j/2.x/)

🟨 [Apache POI](https://poi.apache.org) 

🟨 [ExtentReports 5](https://www.extentreports.com/docs/versions/4/java/index.html)

🟨 [GitHub Actions](https://docs.github.com/en/actions)

## ✳️ Test architecture
🟨 [POM(PageObjectModel)](#-pompageobjectmodel)

🟨 [Reports](#-reports)

🟨 [ScreenShots](#-screenShots)

🟨 [Config](#-config)

🟨 [Driver](#-driver) 

🟨 [Listeners](#-listeners) 

🟨 [PageFactory](#PageFactory) 

🟨 [Util](#Util)

🟨 [Resources](#Resources)

🟨 [Runner](#Runner) 

🟨 [TestComponents](#TestComponents)

🟨 [TestData](#TestData)


### 🟦 POM(PageObjectModel)

**The Page Object Model (POM) is a design pattern commonly used in test automation to enhance the maintainability and reusability of automated tests. It provides a structured way to represent the web pages of an application as objects in the test code.**

####  Benefits of POM:

#### 🟨 Modularity: 

POM divides the application into manageable, modular components, making it easier to create and maintain tests.

#### 🟨 Reduced Code Duplication:

 Reusable Page Objects reduce code duplication across test cases, leading to more efficient test development.

#### 🟨 Enhanced Collaboration:

 Testers and developers can collaborate effectively as they work with well-defined Page Objects.

#### 🟨 Scalability:

 POM scales well with growing test suites, ensuring maintainability as the project evolves.

#### 🟨 Improved Debugging:

 Isolating issues to specific Page Objects simplifies the debugging process.

**In summary, the Page Object Model (POM) is a design pattern that promotes a structured and maintainable approach to web test automation. By representing web pages as Page Objects, it enhances code readability, reusability, and maintainability while reducing code duplication.**

### 🟦 Reports

**The "Reports" folder is a dedicated directory within a test automation project that serves as a repository for various types of test reports. It plays a crucial role in documenting and tracking the results of automated tests. Within this folder, you'll  find two important types of files:**

#### 1. logs.log

Log files, denoted with the ".log" extension, are text-based records of events, activities, and messages generated during the execution of automated tests. These logs provide valuable insights into the test execution process.

#### 2. report.html

The "report.html" file is a comprehensive and visually appealing test report generated by the ExtentReports framework. It serves as a vital component in test automation for documenting and presenting the results of automated test executions. Key features of the "report.html" file include:

#### 🟨 Test Execution Summary

**The report begins with a high-level summary of the test execution, providing essential details such as the total number of test cases `executed`, the number of `passed` and `failed` tests, and the overall pass percentage. This summary offers a quick overview of test suite health.**

#### 🟨 Detailed Test Case Results

**For each individual test case, the "report.html" file provides a detailed breakdown of results, including:**

- Test Case Description: A clear and concise description of the test case.

- Test Status: The status of the test case, indicating whether it `passed` or `failed`.

- Start and End Times: Timestamps indicating when the test case execution began and ended.

- Logs and Steps: A step-by-step account of the test case's actions and expected outcomes.

- Screenshots: If configured, the report includes screenshots captured during test execution, providing visual evidence of test behavior.

### 🟦 ScreenShots

**Folder "ScreenShots" contains screenshots from various types of tests, including tests that have `passed` , been `skipped`, or `failed`. These screenshots are stored in a single shared folder, rather than separately for each type of test.**

### 🟦 Config

**The "Config" folder contains the "GlobalConst.java" file and the "GlobalData.properties" file, which hold global settings and constants used in the application or project. Here is a brief description of the contents of this folder:**

#### 1. GlobalConst.java: 

The "GlobalConst.java" file is a Java class that contains global constants and variables used throughout the project or application. These constants  include items such as `file paths`, `waits time`, `browser config`, `IRetryAnalyzer count`.Storing these constants in one place makes it easier to manage and update them as needed.

#### 2. GlobalData.properties:

 The "GlobalData.properties" file is a properties file that contains global configurations and data in a key-value format. It can include configuration parameters such as `environment settings`, `author name`, `tested page URL`. It serves as an external configuration file that can be easily edited without the need to modify the application's source code. This allows for changes in configuration to be made without the need for recompilation.

**The "Config" folder is used to centralize global settings and data, making it easier to manage and ensuring consistency throughout the project.**


### 🟦 Driver

**The "Driver" folder contains BrowserFactory class is responsible for initializing and configuring web browsers for testing purposes. Here's a brief description of its main functions:**

#### 🟨 initializeDriver()

 This method initializes and configures a web browser based on the provided settings. It returns a WebDriver instance that will be used to perform operations in the browser.

```bash
String browserName = System.getProperty("browser")!=null ? System.getProperty("browser"): `ConfigReaderUtil.getProperty("browser");
```

 This line of code reads the browser value (`browser`) from the system parameter (`if provided as a runtime argument`) or from the configuration file `ConfigReaderUtil.getProperty("browser")`.

#### 🟨 Initialization of Browsers:

`For Chrome:` The WebDriverManager tool is used to manage the Chrome driver. A ChromeDriver instance is created with specified options, such as headless mode, window maximization, etc.

`For Edge:` The WebDriverManager tool is used to manage the Edge driver. An EdgeDriver instance is created with appropriate options.

`For Firefox:` The WebDriverManager tool is used to manage the Firefox driver. A FirefoxDriver instance is created with specified options.

`Browser Options Configuration:`
For each browser, options such as headless mode, window maximization, disabling extensions, etc., can be configured based on test requirements.
```bash

driver.manage().deleteAllCookies(): //Deletes all browser cookies to ensure a clean session.

driver.manage().timeouts().pageLoadTimeout(Duration.ofSeconds(GlobalConsts.PAGE_LOUD_TIME)): //Sets the maximum wait time for page loading.

driver.get(url): //Opens the SeleniumEasy web page in the browser.
```

**This class allows for flexible management of different browsers and configuration options to tailor tests to project needs. It is useful to avoid code duplication and simplifies browser management in Selenium tests.**


### 🟦 Listeners


**The Listener class, located in the "Listeners" folder, is an implementation of TestNG Listeners responsible for monitoring and reporting on the execution of test cases. Here's a summary of its main functions:**


#### 🟨 Setup and Configuration:

The class initializes and configures essential tools and utilities for test monitoring, including `Extent Reports` for test reporting, `logger` for logging, and utilities for taking `screenshots`.

#### 🟨 Test Execution Start (onTestStart):

 When a test case starts, it creates an Extent Test instance associated with the `test method's name`, assigns an `author`, and `logs` the test start. If configured, it takes a `screenshot`.

#### 🟨 Test Execution Success (onTestSuccess):

 In case of a test success, it `logs` the test as `"PASS"` and captures a `screenshot` if configured.

#### 🟨 Test Execution Failure (onTestFailure):

 In the event of a test failure, it logs the test as `"FAIL"` records the failure details, and captures a `screenshot` if configured.

#### 🟨 Test Execution Skipped (onTestSkipped):

 When a test is skipped, it `logs` the test as `"SKIP"` and captures a `screenshot` if configured.

#### 🟨 Test Suite Start (onStart) and Finish (onFinish):

These methods provide information about the `start` and `finish` of the entire `test suite`, and they also `flush the extent reports`.

#### 🟨 Logging and Reporting:

The class makes use of `logger utilities` for detailed `logging` and `Extent Reports` for generating test reports.

**This class plays a vital role in monitoring and reporting on test executions, making it easier to identify test status and any issues during testing. It allows for the efficient capture of screenshots and logging of test results, contributing to better test management and reporting.**



### PageFactory

### Util

### Resources

### Runner

### TestComponents

### TestData



 ## ✳️ Running Tests

To run Regression tests, run the following command

```bash
  mvn test -PRegression
```
To run Smoke tests, run the following command

```bash
  mvn test -PSmoke
```
To run  tests on Edge browser, run the following command

```bash
  mvn test -Dbrowser=edge
```
To run Smoke tests on Chrome browser with Headless mode, run the following command

```bash
  mvn test -PSmoke -Dbrowser=chromeheadless
```







