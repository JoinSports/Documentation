# JoinSports
# Software Architecture Document

## 1. Introduction
### 1.1 Purpose
This document provides a comprehensive architectural overview of the system, 
using a number of different architectural views to depict different aspects of the system. 
It is intended to capture and convey the significant architectural decisions which have been made on the system.

### 1.2 Scope
The scope of this document applies to the JoinSports-App and affects implementation of all use-cases.

### 1.3 Definitions, Acronyms, and Abbreviations
- MVP: Model View Presenter
- UC: Use Case

### 1.4 References
- [Use Cases](https://github.com/JoinSports/Documentation/tree/master/Use%20Cases) of the JoinSports-App

### 1.5 Overview
(n/a)

## 2. Architectural Representation
The app uses the default approach of Android under Java. It is a MVP-like architecture. The view under Android Java
delevelopment stays the view. An Android Activitiy will be used as the Presenter. And custom classes will 
be used as models for handling data.

## 3. Architectural Goals and Constraints
The MVC architecture provides seperation of concerns. The views handle what to render. The Activities respond to the user
input and handles the response of the view to the user and performs actions with the model. The model stores the data and
provides operations on that data as well as performing database operations.

### 3.1 Patterns

We are using the default MVP of Android as base. Because we needed more options we created our own pattern to access the database. Below you can see a part of the class diagram. It clearly show where the way is leading to. We are using a DAO Pattern which means “direct access object”. We introduced for each database object a new class which implements our DAO pattern.

![patterns][]

## 4. Use-Case View
![UCView][]

## 5. Logical View
### 5.1 Overview
![ClassDiagram][]
<!-- ###5.2 Architecturally Significant Design Packages -->

## 6. Process View
n/a

## 7. Deployment View
![Deploy][]

## 8. Implementation View
* The android app uses the web API to gain data about the other users and teams.
* The Web API is only hosted on one server and can be accessed by all Android clients.

## 9. Data View
![erm][]

## 10. Size and Performance
The app should work for up to 100 concurrent users at the moment. The scaling is working pretty good so a larger userbase will be no problem. The performance could be improved by using more caching on the web API and using multiple servers as load balancers.

## 11. Quality
We are using automated testing for the android app. Each commit is build with TravisCI and gets a code coverage report on coveralls. The contributers of the project can see the coverage increase/decrease at merge and pull requests.
![mergepic][]

<!-- picture links -->
[patterns]: https://github.com/JoinSports/Documentation/raw/master/Final%20Presentation/Class%20Diagram%20(DAO%20Pattern).png
[mergepic]: https://github.com/JoinSports/Documentation/raw/master/Testing/TravisCoverallsMerge.png
[erm]: https://github.com/JoinSports/Documentation/raw/master/Final%20Presentation/erm_neu.PNG
[Deploy]: https://github.com/JoinSports/Documentation/raw/master/Final%20Presentation/Deployment%20VIew.png
[UCView]: https://github.com/JoinSports/Documentation/raw/master/UC%20Diagram/use-case%20diagram-newscope.png
[ClassDiagram]: https://github.com/JoinSports/Documentation/raw/master/Final%20Presentation/class-diagramm-marked.png
