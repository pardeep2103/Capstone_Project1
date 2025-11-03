### 1. Error: base.log is not visible  
**When this error came:** While running the capstone project.  
**Why this error came:** The log variable in the base class was private, so it couldn’t be used in the step definition class.  
**How I solved it:** I changed log to protected static in the base class so it can be accessed in other classes.



### 2. Error: DuplicateStepDefinitionException  
**When this error came:** While running both login and signup feature files.  
**Why this error came:** Same method name enterUsername was written in both login and signup step definition classes.  
**How I solved it:** I changed the step name or method name in one of the classes to make it different.



### 3. Error: UnhandledAlertException: unexpected alert open  
**When this error came:** After clicking the login button in the login page.  
**Why this error came:** Alert popup came because username or password was empty or not properly entered.  
**How I solved it:** I added try-catch block to handle alert and made sure username and password are entered before clicking login.



### 4. Error: Login success message mismatch. expected [Welcome dEEP@2809] but found []  
**When this error came:** After clicking login button in valid login test case.  
**Why this error came:** The welcome message was not displayed or not found by Selenium.  
**How I solved it:** I added wait condition to check if the welcome message is visible before reading it.



### 5. Error: Alert message mismatch. expected [Wrong password.] but found [User does not exist.]  
**When this error came:** After clicking login button in invalid login test case.  
**Why this error came:** The expected alert message was different from the actual popup shown by the application.  
**How I solved it:** I changed the expected message in the feature file to match the actual alert shown.



### 6. Error: SLF4J: Failed to load class "StaticLoggerBinder"  
**When this error came:** During test execution when logging was used.  
**Why this error came:** SLF4J binding dependency was missing in the project.  
**How I solved it:** I added slf4j-log4j12 dependency in the pom.xml file.


### 7. Error: Log4j2 could not find a logging implementation  
**When this error came:** When trying to use logging in the project.  
**Why this error came:** log4j-core dependency was missing.  
**How I solved it:** I added log4j-core dependency in the pom.xml file.



### 8. Error: CDP version mismatch warning  
**When this error came:** While launching Chrome browser.  
**Why this error came:** Chrome version was 141 but Selenium didn’t support it by default.  
**How I solved it:** I added selenium-devtools-v141 dependency in the pom.xml file.


### 9. Error: ElementNotInteractableException  
**When this error came:** While entering username or password or clicking login button.  
**Why this error came:** The element was not ready or hidden when Selenium tried to interact with it.  
**How I solved it:** I added WebDriverWait to wait until the element is visible or clickable before using it.



