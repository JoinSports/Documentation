# JoinSports
# Use-Case Specification: Delete team

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the administrator of a team (leader) to delete his existing team. 
After this selection all relations of other users (members) to this team are removed too.

## 2. Flow of Events
### 2.1 Basic Flow 
The team leader select the option to delete his team within the team mode.

#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature files
<!-- ![Feature] -->

Deletion successful:
```cucumber
Feature: Delete team
  As a team leader
  I want to delete my team
 	Scenario: deletion of the team successful (normal execution)
    Given the user is logged in in his account and entered the team mode
    When the delete button in the team mode menu is clicked
    Then team is deleted (relation to this team is removed for all team members)
```

Internal server error:
```cucumber
Feature: Delete team
  As a team leader
  I want to delete my team
 	Scenario: problem during the connection to the server (server or internal error)
    Given the user is logged in in his account and entered the team mode
    When the delete button in the team mode menu is clicked
    Then the feedback shows "Internal server error, please try again later or contact our support team!"
          [a) The User can wait until the issues are fixed
           b) The User can ask to the support team if the problem remains]
```

### 2.2 Alternative Flows
#### 2.2.1 Team not deleted 
Because of problems during the connection to the server the deletion failed.

## 3. Special Requirements
n/a

## 4. Preconditions
The user must be logged in to his JoinSports account and must be the team leader.

## 5. Postconditions
### 5.1 Team deleted
The team leader has deleted the team and is forwarded to main page of an normal user.
(In the team mode does not exist a team relation any more. But the user is allowed to create a new team and invite members.)

### 5.2	Team not deleted
If there were problems during the connection to the server the deletion failed.

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: ? "UML Diagram"
[Mock]: ? "Mock-Up"
<!-- [Feature]:  "Feature file" -->
