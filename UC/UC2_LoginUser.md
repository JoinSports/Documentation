#JoinSports
#Use-Case Specification: Login user

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the user to login to his account of the JoinSports application.

## 2. Flow of Events
### 2.1 Basic Flow 
The user entered his login data (username & password). The system checks, whether the combination is correct.
If the combination exists in the database of the system, the user is logged in with his user account. The application forwards the user to the start page.
Otherwise the application print out an error message that either username or password is wrong. In this case the user has to correct his login data and try to login again.

#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature files
![Feature]

Correct login:
```cucumber
Feature: Login user
  As a unknown user
  I want to login to my user account
 	Scenario: correct login (normal execution)
    Given the entered username is 'TestUser' and the password is 'MyPassword123'
    When the login button is clicked
    Then the user is logged in and is forwarded to the main page
```
Username invalid:
```cucumber
Feature: Login user
  As a unknown user
  I want to login to my user account
 	Scenario: username does not exist in the system database
    Given the entered username is 'aNotExistingUsername'
    When the login button is clicked
    Then the login failed and a message “Invalid username, the username does not exist!” is shown
```

Password incorrect:
```cucumber
Feature: Login user
  As a unknown user
  I want to login to my user account
 	Scenario: username correct, but wrong password
    Given the chosen username is 'TestUser'
    When the login button is clicked
    Then the login failed and a message “Incorrect password, please try to login again!” is shown
```

Internal server error:
```cucumber
Feature: Login user
  As a unknown user
  I want to login to my user account
 	Scenario: problem during the registration (server or internal error)
    Given the chosen combination is a correct expression
    When the login button is clicked
    Then the feedback shows “Internal server error, please try again later or contact our support team!”
          [a) The User can wait until the issues are fixed
           b) The User can ask to the support team if the problem remains]

```

### 2.2 Alternative Flows
#### 2.2.1 Login data is incorrect
If the entered combination of username and password is incorrect, show an error message to the user that either username or password is wrong.
(In this case the user has to correct his login data and try to login again.)

## 3. Special Requirements
n/a

## 4. Preconditions
The JoinsSport application must be installed and executed on a Android device.

## 5. Postconditions
### 5.1 User logged in
The user is logged in with his user account. The application forwards the user to the start page.
The user is now allowed to use the funtionality of an normal user within the JoinSports application.

### 5.2	User not logged in
If the combination of username and password is incorrect the login process failed. The user has to try it again wih different login data. 

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: ? "UML Diagram"
[Mock]: ? "Mock-Up"
<!-- [Feature]:  "Feature file" -->
