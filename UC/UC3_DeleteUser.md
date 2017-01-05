#JoinSports
#Use-Case Specification: Delete user

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the user to delete his user account which he has already created.

## 2. Flow of Events
### 2.1 Basic Flow 
The user select the option to delete his account within the settings menu. 

#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature files
<!-- ![Feature] -->

Correct login:
```cucumber
Feature: Delete user
  As a normal user
  I want to delete my user account
 	Scenario: deletion of the user account successful (normal execution)
    Given the user is logged in in his account and entered the settings menu
    When the delete button in the settings menu is clicked
    Then user account is deleted (no login possible any more in future)
```

Internal server error:
```cucumber
Feature: Delete user
  As a normal user
  I want to delete my user account
 	Scenario: problem during the connection to the server (server or internal error)
    Given the user is logged in in his account and entered the settings menu
    When the delete button in the settings menu is clicked
    Then the feedback shows "Internal server error, please try again later or contact our support team!"
          [a) The User can wait until the issues are fixed
           b) The User can ask to the support team if the problem remains]
```

### 2.2 Alternative Flows
#### 2.2.1 User not deleted 
Because of problems during the connection to the server the deletion failed.

## 3. Special Requirements
n/a

## 4. Preconditions
The user must be logged in to his JoinSport account.

## 5. Postconditions
### 5.1 User account deleted
The user has deleted his account and is forwarded to th login/registration page.

### 5.2	User account not deleted
If there were problems during the connection to the server the deletion failed.

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: ? "UML Diagram"
[Mock]: ? "Mock-Up"
<!-- [Feature]:  "Feature file" -->
