#JoinSports
#Software Architecture Document

##1. Introduction
###1.1 Purpose
This document provides a comprehensive architectural overview of the system, 
using a number of different architectural views to depict different aspects of the system. 
It is intended to capture and convey the significant architectural decisions which have been made on the system.

###1.2 Scope
The scope of this document applies to the JoinSports-App and affects implementation of all use-cases.

###1.3 Definitions, Acronyms, and Abbreviations
- MVP: Model View Presenter
- UC: Use Case

###1.4 References
- [Use Cases](https://github.com/JoinSports/Documentation/tree/master/UC) of the JoinSports-App

###1.5 Overview
(n/a)

##2. Architectural Representation
The app uses the default approach of Android under Java. It is a MVP-like architecture. The view under Android Java
delevelopment stays the view. An Android Activitiy will be used as the Presenter. And custom classes will 
be used as models for handling data.

##3. Architectural Goals and Constraints
The MVC architecture provides seperation of concerns. The views handle what to render. The Activities respond to the user
input and handles the response of the view to the user and performs actions with the model. The model stores the data and
provides operations on that data as well as performing database operations.

##4. Use-Case View
(n/a)

##5. Logical View
###5.1 Overview
![ClassDiagram][]
###5.2 Architecturally Significant Design Packages

##6. Process View
(n/a)

##7. Deployment View
to be determined

##8. Implementation View
(n/a)

##9. Data View
to be determined

##10. Size and Perforance
(n/a)

##11. Quality
(n/a)

<!-- picture links -->
[ClassDiagram]: https://github.com/JoinSports/Documentation/blob/master/Class-diagram-UML/ClassDiagram_UML_cut.jpeg?raw=true
