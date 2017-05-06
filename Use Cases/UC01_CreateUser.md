# JoinSports
# Use-Case Specification: Create user

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the user to create a new account within the JoinSports application.

## 2. Flow of Events
### 2.1 Basic Flow 
The user specifies his personal user data. The system checks, whether the username already exists or if the user data fullfill the requirements. 
If the username is not taken and the user data are correct, create the user account and notify the user has been successfully created. 
Otherwise print out an error message that the user account could not be created. In this case the user has to correct his user data and confirm them again. 

#### 2.1.1 UML diagram
![UML diagram][UML]

#### 2.1.2 Mockup 
![Mockup][Mock]

#### 2.1.3 Feature file
<!-- ![Feature] -->

Correct registration:
```cucumber
Feature: Create user
  As a unknown user
  I want to create a new user account
 	Scenario: correct registration (normal execution)
    Given the chosen username is 'TestUser'
    When the create user button is clicked
    Then a new user account is created and a message “User successfully created!” is shown
```
Username invalid:
```cucumber
Feature: Create user
  As a unknown user
  I want to create a new user account
 	Scenario: username has wrong characters or is too short/long
    Given the chosen username is 'ABC'
    When the create user button is clicked
    Then the registration failed and a message “Invalid username, please specify a correct username!” is shown
```

Username unavailable:
```cucumber
Feature: Create user
  as a unknown user
  I want to create a new user account
 	Scenario: problem during the registration (name already taken)
    Given the chosen username is 'TestUser'
    When the create user button is clicked
    Then the feedback shows “Username unavailable, please try again with another name!”
          [a) The User should give another name, starting the Use Case again.
           b) The User can abort.]

```

Internal server error:
```cucumber
Feature: Create user
  As a unknown user
  I want to create a new user account
 	Scenario: problem during the registration (server or internal error)
    Given the chosen username is a correct expression
    When the create user button is clicked
    Then the feedback shows “Internal server error, please try again later or contact our support team!”
          [a) The User can wait until the issues are fixed
           b) The User can ask to the support team if the problem remains]

```


### 2.2 Alternative Flows
#### 2.2.1 Username is already taken
If username is taken, which the user entered, show an error message to the user that the user account could not be created. End of flow.
(In this case the user has to correct his user data and confirm them again.)

## 3. Special Requirements
n/a

## 4. Preconditions
The JoinsSport application must be installed and executed on a Android device.

## 5. Postconditions
### 5.1 User created
The user has created an user account and is now allowed to use the funtionality of an normal user within the JoinSports application.

### 5.2	User not created
If an error occurs the user account will not be created.  (example: username already in use)

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: https://github.com/JoinSports/Documentation/blob/master/Class-diagram-UML/ClassDiagram_UML_cut.jpeg "UML Diagram"
[Mock]: ? "Mockup"
<!-- [Feature]:  "Feature file" -->
