# JoinSports
# Use-Case Specification: <UC>

## 1. Use-Case Name 
### 1.1 Brief Description
This use case queries a all existing team names from the database.

## 2. Flow of Events
### 2.1 Basic Flow 
The user wants to see all existing teams. The application queries a all existing team names. If the database access was successful, the application shows all team names on the screen.

#### 2.1.1 UML diagram
![UC diagram][UC]

#### 2.1.2 Mockup 
![Mockup][Mock]

#### 2.1.3 Feature file
<!-- ![Feature] -->

<Case 1>:
```cucumber
Feature: Read All Unjoined Teams
  As a normal user
  I want to show all existing teams
 	Scenario: Database query successful
    Given the user is logged in to his account
    When the user opens the "Teams finden" menu in the Navigation Bar to show his personal user data
    Then a list of all teams is printed to the screen
```
<Case 2>:
```cucumber
Feature: Read All Unjoined Teams
  As a normal user
  I want to show all existing teams
 	Scenario: Database query returns error
    Given the user is logged in to his account
    When the user opens the "Teams finden" menu in the Navigation Bar to show his personal user data
    Then an error message is shown to the user
```


### 2.2 Alternative Flows
#### 2.2.1 <Case>
If the database query of the requested team data sets returns an error message, show an error message to the user on the screen. End of flow. (In this case the user may try it again later.)

## 3. Special Requirements
n/a

## 4. Preconditions
The JoinsSport application must be installed and executed on a Android device.

## 5. Postconditions
### 5.1 All team names visible
The user can see a list of all existing team names on the screen.

### 5.2	All team names not visible
If an error occurs the user can not see the list of existing team names. Instead he can see an error message that database connection was unsuccessful.

## 6. Extension Points
n/a

<!-- picture links -->
[UC]: ? "UML Diagram"
[Mock]: ? "Mockup"
<!-- [Feature]:  "Feature file" -->
