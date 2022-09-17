
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

|                 | Description UC01                                          
|-----------------|-------------------
| Name:           | 
| Actor:          | 
| Description:    | 
| Pre-Condition:  | 
| Scenario:       | 
| Result:         | 
| Extensions:     | 
| Exceptions:     | 

|                 | Description UC02                                          
|-----------------|-------------------
| Name:           | 
| Actor:          | 
| Description:    | 
| Pre-Condition:  | 
| Scenario:       | 
| Result:         | 
| Extensions:     | 
| Exceptions:     | 

|                 | Description UC03                                          
|-----------------|-------------------
| Name:           | 
| Actor:          | 
| Description:    | 
| Pre-Condition:  | 
| Scenario:       | 
| Result:         | 
| Extensions:     | 
| Exceptions:     | 

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
| Name:           | 
| Actor:          | 
| Description:    | 
| Pre-Condition:  | 
| Scenario:       | 
| Result:         | 
| Extensions:     | 
| Exceptions:     | 