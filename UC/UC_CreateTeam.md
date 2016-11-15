#JoinSports
#Use-Case Specification: Create team

## 1. Use-Case Name 
### 1.1 Brief Description
This use case will allow the user to create a new team.

## 2. Flow of Events
### 2.1 Basic Flow 
The user specifies the team name which what he wants to create a team. The system checks, whether the team name already exists. 
If the name is not taken, create the team and notify the team has been successfully created.
#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature file
![Feature]

Correct register:
```
Feature: Create Team
  as a User
  I want to create a new team
 	Scenario: correct registration, normal execution
    Given: The chosen team name is “TeamTest”
    When: the create team button is clicked
    Then: a new team is created and a message “Team successfully created!” is shown
```
Team name invalid:
```
Feature: Create Team
  as a User
  I want to create a new team
 	Scenario: team name has wrong characters or is too short/long
    Given: The chosen team name is “ABC”
    When: the create team button is clicked
    Then: a new team is created and a message “Team successfully created!” is shown
```

Team name unavailable:
```
Feature: Create Team
  as a User
  I want to create a new team
 	Scenario: problem during the registration (name already taken)
      	Given: The chosen team name is “TeamTest”
      	When: the create team button is clicked
      	Then: the feedback shows “Name unavailable, please try again with another name!”
              [a) The User should give another name, starting the Use Case again.
               b) The User can abort.]

```

Internal server error:
```
Feature: Create Team
  as a User
  I want to create a new team
 	Scenario: problem during the registration (server or internal error)
    Given: The chosen team name is a correct expression
    When: the create team button is clicked
    Then: the feedback shows “Internal server error, please try again later or contact our support team!”
          [a) The User can wait until the issues are fixed.
           b) The User can ask to the support team if the problem remains]

```


### 2.2 Alternative Flows
#### 2.2.1 Team name is taken
If team name is taken, which the user entered, show an error message to the user. End of flow.

## 3. Special Requirements
n/a

## 4. Preconditions
none

## 5. Postconditions
### 5.1 Team created
the team was successfully created
### 5.2	Team not created
if error occurs the team will not be created  (example: team name already in use)
## 6. Extension Points
n/a

<!-- picture links -->
[UML]: https://github.com/JoinSports/Documentation/blob/master/UC/Create%20Team.png "UML Diagram"
[Mock]: https://github.com/JoinSports/Documentation/blob/master/UC/Mockup%20create%20team.png "Mock-Up"
<!-- [Feature]:  "Feature file" -->
