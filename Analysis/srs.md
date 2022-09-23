# Software Requirements Specification for tennis scorekeeping application

Authors: James Boogaard, Hendrik Paß, Jan Pinto Strohhäusl, Justus Reiffs, Tim Baars and Tom Jacobs <br>
Customer: Tennis Club 
 
# 1 Introduction 

This Software Requirements Specification document outlines the group Tennis Club 2’s solution to the client’s need to replace their old tennis score keeping system as well as making it more efficient to record and fetch data from tennis matches. The topics covered in this document include: an 
introduction to the client’s problem, the team’s proposed solution to address the problem such as how the product system should function, specific system and client requirements, and diagrams illustrating use cases and scenarios when the system would be used. 

## 1.1 Purpose 

The Software Requirements Specification (SRS) document serves to outline the technical requirements needed by the developers working on creating the system for keeping track of tennis scores and storing the results digitally. This document provides specific insight such as requirements, constraints, and detailed explanations of the proposed system to combat the client’s problem. 

## 1.2 Scope 

The system will be an offline application that has the ability to add scores to one of two players, it also allows for the addition of names and the clubs those names belong to. The application will then require an internet connection to upload the information to the database after the match is completed. 

## 1.3 Definitions, acronyms, and abbreviations 

| *Word / Abbreviation*              | *Definition*
|---------------|------------------------
| SRS (Software Requirements Specification) | A document of the software system to be developed that discusses the functional and nonfunctional requirements. It also includes use cases that describe how users (client analysts) would interact with the software. 
| Love | In tennis love is used to describe a score of zero. 
| Advantage (adv.) | Given as a score when they win the next point after a game goes to a deuce.
| Deuce | A deuce is when both sides have a score of 40. This means that they are now two points away from winning the game. 
| Database | Is an organized collection of structured information that in our case will be used to store the past games information.

## 1.4 References
Title : HOW DOES TENNIS SCORE WORK? TENNIS SCORE EXPLAINED <br>
Report Number : - <br>
Date : April 30, 2022 <br>
Publishing Organization : Super Tennis Racquet - Robert Dexter <br>
https://supertennisracquet.com/how-does-tennis-score-work/

Title : TENNIS RANKING SYSTEM: HOW DOES IT WORK? WTA & ATP EXPLANATIONS <br>
Report Number : - <br>
Date : January 1, 2022 <br>
Publishing Organization : Super Tennis Racquet - Robert Dexter <br>
https://supertennisracquet.com/tennis-ranking-system/

## 1.5  Overview

Following this introductory section, the rest of the Software Requirements Specification document will further explain the specifics of the software system being produced. Chapter 2 focuses on the context for the proposed system, how it should function, and the related constraints. Chapter 3 provides a detailed listing of the requirements specific to the system following a hierarchical numbering scheme.

# 2 Overall Description 

This section will cover general information about the project perspective, functions, and various requirements and constraints.
 
## 2.1 Product Perspective 

This product is used to track information for tennis games and then store that information in a database where it can later be accessed and efficiently sorted through. It will also lead to the information being safer as there is now risk as you can duplicate the information more easily. It will be an application that can be used offline and then when it has internet connection again it will upload the information to the database to be safely stored. 

## 2.2 Product Functions 

The end product will start off by having an initialization for a match option where the user can then enter all the information about the players and their clubs that is needed and then they start the match where they can update information like the scores as well as the names if needed. They then end the match, and the data is stored locally if there is no internet connection available and is then 
uploaded later when there is a connection. There will also be a search function for users that are not on the admin where they can access information about matches by searching key phrases that are applicable to the matches they want to find. 

## 2.3 User Characteristics 

There are two types of users that will have this program available to them. First, there is the umpire who will have access to starting, ending and updating scores and names during the course and before a match. Second, are the other users who use the application but only have access to the search function so they are able to find matches from the past and access those match’s information. 

## 2.4 Constraints 

The system only requires that in order to upload the information of a match once it is finalized it will need an internet connection.  

## 2.5 Assumptions and Dependencies 

It is assumed that the end user will have access to an internet connection at some point during or after the match, they must also have access to a phone or tablet or device capable of connecting to the internet. They should also know the rules of tennis if they are to be adding scores in one of the admin accounts. 
 
 

3. Specific Requirements
3.1 External Interface Requirements
3.1.1 User Interfaces
3.1.2 Hardware Interfaces
3.1.3 Software Interfaces
3.1.4 Communication Interfaces
 
3.2 System Features
3.2.1 System Feature 1 (Search Match)
3.2.1.1 Introduction/Purpose of Feature
3.2.1.2 Stimulus/Response Sequence
3.2.1.3 Associated Functional Requirements
---
### 3.2.2 System Feature 2 (View Match)
### 3.2.2.1 Introduction/Purpose of Feature

It enables a user to look at the data(The score, The rounds and Player name and club) for a match that has taken place.

### 3.2.2.2 Stimulus/Response Sequence
    
### 3.2.2.3 Associated Functional Requirements
---
### 3.2.3 System Feature 3 (Initiate Match)
#### 3.2.3.1 Introduction/Purpose of Feature
This feature is a key feature of this software. With this feature, a new match instance shall be created and made available for now or later use.
The match shall contain the following information:
- Club Names
- Match Date
- Sets required to win

Optionally the match can contain:
- Team (e.g. U17-1 for age under 17 team 1, U17-2 for age under 17 team 2)
- Player Name (As GDPR )

#### 3.2.3.2 Stimulus/Response Sequence
3.2.3.2.1 Actor selects option to initiate new match <br />
3.2.3.2.2 System requests Actor to provide match data (Club names, match date, sets to win) <br />
3.2.3.2.3 Actor provides match data (Club Names, match date, sets to win) <br />
3.2.3.2.4 Actor selects to create match <br />
3.2.3.2.5 System adds new match

#### 3.2.3.3 Associated Functional Requirements
3.2.3.3.1 Actor must have Referee or higher permissions <br />
3.2.3.3.2 Actor must provide valid information <br />
3.2.3.3.3 Invalid Date results in now

---

### 3.2.4 System Feature 4 (Finalize Match)

3.2.4.1 Introduction/Purpose of Feature

This feature is a key feature of this software. With this feature, the match data given by the referee through out the match will be collected and directly uploaded to the database. In the database the data will be stored and be available for everyone. This way it is ensured that the data will be stored correctly in the database and will not be changed during the process of archiving.

3.2.4.2 Stimulus/Response Sequence

To activate this feature, the referee needs to initiate a match. After that, the referee needs to input data before finalizing the match. After finalizing the match, the match will uploaded to the database and users cannot change the inputted data.

3.2.4.3 Associated Functional Requirements

---
 
### 3.2.5 System Feature 5 (Update Match)
### 3.2.5.1 Introduction/Purpose of Feature
### 3.2.5.2 Stimulus/Response Sequence
### 3.2.5.3 Associated Functional Requirements

 
3.3 Performance Requirements
3.4 Design Constraints
3.5 Software System Attributes
3.6 Other Requirements
