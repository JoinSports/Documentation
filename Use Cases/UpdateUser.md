# JoinSports
# Use-Case Specification: Update user

## 1. Use-Case Name
### 1.1 Brief Description
This use case will allow the user to change some of his personal user account data and send the updated information to the server.

## 2. Flow of Events
### 2.1 Basic Flow 
The user select the option to update his user account data within the settings menu. 
After he adjust his user data he pressed the update button to send save the information on the server. 

#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature files
<!-- ![Feature] -->

Update successful:
```cucumber
Feature: Update user
  As a normal user
  I want to update my user account data
 	Scenario: update of the user account data was successful (normal execution)
    Given the user is logged in in his account and entered the settings menu
    When the update button in the settings menu is clicked
    Then user account data is changed
```

Internal server error:
```cucumber
Feature: Update user
  As a normal user
  I want to update my user account data
 	Scenario: problem during the connection to the server (server or internal error)
    Given the user is logged in in his account and entered the settings menu
    When the update button in the settings menu is clicked
    Then the feedback shows "Internal server error, please try again later or contact our support team!"
          [a) The User can wait until the issues are fixed
           b) The User can ask to the support team if the problem remains]
```

### 2.2 Alternative Flows
#### 2.2.1 User not deleted 
Because of problems during the connection to the server the update failed.

## 3. Special Requirements
n/a

## 4. Preconditions
The user must be logged in to his JoinSport account.

## 5. Postconditions
### 5.1 Update of the user data successful
The user has deleted his account and is forwarded to th login/registration page.

### 5.2	Update of the user data failed
If there were problems during the connection to the server the update failed.

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: ? "UML Diagram"
[Mock]: https://github.com/JoinSports/Documentation/blob/master/Mockups/Update%20User.png "Mock-Up"
<!-- [Feature]:  "Feature file" -->
