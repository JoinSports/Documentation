# JoinSports
# Use-Case Specification: Read user

## 1. Use-Case Name 
### 1.1 Brief Description
This use case queries a certain data set from type User in the database.

## 2. Flow of Events
### 2.1 Basic Flow 
The user wants to see his personal settings within the settings menu. 
The application queries the personal information.
If the database access was successful, the application shows the user data on the screen.

#### 2.1.1 UML diagram
![UC diagram][UC]

#### 2.1.2 Mockup 
![Mockup][Mock]

#### 2.1.3 Feature file
<!-- ![Feature] -->

Database query successful:
```cucumber
Feature: Read user
  As a normal user
  I want to show my personal user data
 	Scenario: Database query successful
    Given the user is logged in to his account
    When the user opens the settings menu to show his personal user data
    Then the personal information is printed to the screen
```
Database query returns error:
```cucumber
Feature: Read user
  As a normal user
  I want to show my personal user data
 	Scenario: Database query returns error
    Given the user is logged in to his account
    When the user opens the settings menu to show his personal user data
    Then an error message is shown to the user
```


### 2.2 Alternative Flows
#### 2.2.1 Database connection problems
If the database query of the requested user data set returns an error message, show an error message to the user on the screen. 
End of flow.
(In this case the user may try to click the settings menu again or try it later again.)

## 3. Special Requirements
n/a

## 4. Preconditions
The JoinsSport application must be installed and executed on a Android device.
The user must have created an account and logged in at JoinSports. 

## 5. Postconditions
### 5.1 The personal user data visible
The user can see his personal user data on the screen.

### 5.2	The personal user data is not visible
If an error occurs the user can not see his personal user data.
Instead he can see an error message that database connection was unsuccessful.

## 6. Extension Points
n/a

<!-- picture links -->
[UC]: https://github.com/JoinSports/Documentation/blob/master/Class-diagram-UML/ClassDiagram_UML_cut.jpeg "UML Diagram"
[Mock]: ? "Mockup"
<!-- [Feature]:  "Feature file" -->
