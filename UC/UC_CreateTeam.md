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

![Feature]

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
[Feature]:  "Feature file"
