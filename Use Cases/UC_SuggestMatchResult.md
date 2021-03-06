# JoinSports
# Use-Case Specification: Suggest match result

## 1. Use-Case Name 
### 1.1 Brief Description
This use case is for suggest a match result after the end of a match.

## 2. Flow of Events
### 2.1 Basic Flow 
After a match has been finished one of the two team leaders can suggest a match result. 
After that the other team leader can accept or decline this result. 
If the result is accepted the match result is shown public and the points are given. 
If the suggestion was declined the team leader can make a new suggestion to the other leader, 
which must be confirmed the same way as before.

#### 2.1.1 UML diagram
![UML]

#### 2.1.2 Mock-up 
![Mock]

#### 2.1.3 Feature file
![Feature]

Add new result:
```cucumber
Feature: Suggest match result
  As a team leader
  I want add a new match result
  Scenario: There is no result for that match yet (normal execution)
    Given a correct result form a played match  
    When the add result button is clicked
    Then the result is added but not public until the leader of the other team accepts it
```

Edit wrong suggested result:
```cucumber
Feature: Suggest match result
  As a team leader
  I want to edit a wrong  match result
    Scenario: There is a result added by the leader of the other team, but it is not correct
    Given a wrong result from a played match
    When the edit result button is clicked
    Then the user changes the result to the real one but it is not public until the leader of the other team accepts it
```

Accept correct result:
```cucumber
Feature: Suggest match result
  As a team leader
  I want to accept a match result
  Scenario: There is a result added by the leader of the other team and it is correct
    Given a correct result form a played match
    When the accept result button is clicked
    Then the user accepts the result and it is public for all the users
```


### 2.2 Alternative Flows
#### 2.2.1 Suggested result is wrong
If the suggested result is wrong the team leader can edit the result. The new result must also be accepted by the opponents team leader.

## 3. Special Requirements
n/a

## 4. Preconditions
### 4.1 Match finished
The match between two teams has been finished.

## 5. Postconditions
### 5.1 Match result accepted
The result is accepted from both team leaders and the procedure is finished.

### 5.2	Disagreement about the result
There is a missmatch between the sugessted results. 
An Administrator of the JoinSports-Team has to make a decision for further actions.

## 6. Extension Points
n/a

<!-- picture links -->
[UML]: https://github.com/JoinSports/Documentation/blob/master/UC/suggest%20match%20result.png "UML Diagram"
[Mock]: https://github.com/JoinSports/Documentation/blob/master/UC/Mockup%20suggest%20team%20result.png "Mock-Up"
[Feature]:  "Feature file"
