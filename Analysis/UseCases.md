
|                | Description UC01                                                 |
| -------------- | ------------------------------------------------------------ |
| Name:          | Search match data                                              |
| Actor:         | Everyone
| Description:   | Anyone is searching for a match.                                |
| Pre-Condition: | n/a                                   |
| Scenario:      | 1. System asks actor to select a date.<br />2. User actor selects date.<br />3. System shows all matches of that day.	|
| Result:        | The actor can access the match he wants to access.                  |
| Extensions:    | n/a
| Exceptions:    | 2. There is no match on that specific date. <br />2.1 System returns to step 1. |


|                 | Description UC02                                          
|-----------------|-------------------
| Name:           | view match data 
| Actor:          | Everyone
| Description:    | View information about a match
| Pre-Condition:  | A match exists in the database
| Scenario:       | 1. The user selects a match that has taken place.</br>2. The systems displays the match's page and the match's data.
| Result:         | The user can view the data/information of a specific match. 
| Extensions:     | n/a
| Exceptions:     | n/a

|                 | Description UC03           |                               
|-----------------|-------------------|
| Name:           | Initiate Match |
| Actor:          | Referee or Club Management |
| Description:    | Creates a new match |
| Pre-Condition:  | Actor must be signed in as Referee or Club Management |
| Scenario:       | 1. Actor selects option to initiate new match  <br />2. System requests Actor to provide match data (Club names, match date, sets to win) <br />3. Actor provides match data (Club Names, sets to win) <br />4. Actor selects to create match <br />5. System adds new match |
| Result:         | Match was created |
| Extensions:     | 5.a.1 Actor selects advanced match data <br />5.a.2 System requests Actor to provide advanced match data (Player names, Team name) <br />5.a.3 Actor provides advanced match data <br />5.a.4 Actor selects save option <br />5.a.5 Executes step 5. |
| Exceptions:     | 5.a.1 Actor provided incorrect data <br />5.a.2 Returns to step 3. |

|                 | Description UC04                                          
|-----------------|-------------------
| Name:           | Finalize match
| Actor:          | Referee
| Description:    | Referee is finalizing a match.
| Pre-Condition:  | A match was initialized.
| Scenario:       | 1. Actor selects option to close the game. <br />2. System checks given data and asks actor for confirmation. <br />3. Actor confirms. <br />4. System collects given data and uploads data to the database.
| Result:         | The match is closed and uploaded to the database.
| Extensions:     | 3.a Actor does not confirm. <br />1. System goes back and gives actor options to edit the given data.
| Exceptions:     | 2. If not data was given, system informs actor that actor needs to input data. <br />2.1 System returns to step 1.

|                 | Description UC05                                          
|-----------------|-------------------
| Name:           | Updating match
| Actor:          | Referee
| Description:    | Updating scores and player and team information during the course of the match
| Pre-Condition:  | There is an ongoing game available to update.
| Scenario:       | 1. Actor selects ongoing game to update <br> 2. System displays current game information <br> 3. Actor changes team names and/or scores <br> 4. Actor indicates that they want to finalize the match <br> 5. System asks for confirmation <br> 6. Actor confirms <br> 7. System finalizes match information and returns the actor to the match list
| Result:         | A games inforamtion has been updated.
| Extensions:     | N/A
| Exceptions:     | 4. Actor indicates that they're done<br>4.1 Actor has entered an invalid name<br>4.2 System points out invalid text field and returns to step 3.
