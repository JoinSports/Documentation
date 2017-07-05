# JoinSports
# Use-Case Specification: Update team

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the team leader to change some of the team data and send the updated information to the server.

## 2. Flow of Events
### 2.1 Basic Flow 
The team leader select the option to update the team data within the settings menu. After he adjust the team data he pressed the update button to save the information on the server.

#### 2.1.1 UML diagram
![UC diagram][UC]

#### 2.1.2 Mockup 
![Mockup][Mock]

#### 2.1.3 Feature file
<!-- ![Feature] -->

<Case 1>:
```cucumber
Feature: Update team
  As a team leader
  I want to update the team data
 	Scenario: update of the team data was successful (normal execution)
    Given the user is logged in in his account, is a team leader and entered the team settings menu
    When the update button in the team settings menu is clicked
    Then team data is changed
```
<Case 2>:
```cucumber
Feature: Update team
  As a team leader
  I want to update the team data
 	Scenario: problem during the connection to the server (server or internal error)
    Given the user is logged in in his account, is a team leader and entered the team settings menu
    When the update button in the team settings menu is clicked
    Then an error message is shown
```


### 2.2 Alternative Flows
#### 2.2.1 Team not updated
Because of problems during the connection to the server the update failed.

## 3. Special Requirements
n/a

## 4. Preconditions
The JoinsSport application must be installed and executed on a Android device.
The user must be logged in to his JoinSport account and has to be a team leader.

## 5. Postconditions
### 5.1 Update of the team data successful
The team leader has updated his account data.

### 5.2	Update of the team data failed
If there were problems during the connection to the server the update failed.

## 6. Extension Points
n/a

<!-- picture links -->
[UC]: ? "UML Diagram"
[Mock]: ? "Mockup"
<!-- [Feature]:  "Feature file" -->
