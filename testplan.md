Feature: Single Bet Placement

Scenario 1: Single Bet Validation
ID: S01
Title : Place a single bet
Priority : Critical
Risk Rationale : It's a core business flow if broken user can't place a bet or may be mislead due to wrong results and it impacts the revenue
Steps : 
step 1 - Navigate to match list 
step 2 - Select date and odds range if want shorter or refined list
step 3 - Select a specific odds for a specific match
step 4 - Enter stake at right side
step 5 - Click on "PLACE BET" button
Expected Result :
1) Once placed successfully then it should show Success receipt with Bet ID, Match details, Selection, Stake, Odds, Potential payout, Placement timestamp 
2) When Success receipt closed then show reduced balance for the user 


Scenario 2: Match list filters
ID: S02
Title : Match list working according to filters
Priority : High
Risk Rationale : If displays wrong dates or odds or past events then user can bet on wrong match and lose money 
Steps : 
step 1 - Navigate to match list (it will show all upcoming matches)
step 2 - Select a date or range of dates
step 3 - Select min and maximum odds
Expected Result :
1) As select a date or range of dates then it should show inclusive dates upcoming matches
3) min = 1.01 and max = 1000.00 , user should not be able to select below or beyond that

Scenario 3: Minimum stake
ID: S03
Title : User enetered less than €1.00 and user balance is €120.00
Priority : High
Risk Rationale : Invalid bet can be placed if no validation or if user is not blocked
Steps : 
step 1 - Navigate to match list 
step 2 - Select a specific odds for a specific match
step 4 - Enter stake at right side €0.25
step 5 - Click on "PLACE BET" button
Expected Result :
1) Show validation message "Minimum stake is €1.00"
2) Should not be able to place a bet


Scenario 4: Maximum stake
ID: S04
Title : User enetered more than €100.00 and user balance is €120.00
Priority : High
Risk Rationale : Invalid bet can be placed and risk more money if no validation or if user is not blocked
Steps : 
step 1 - Navigate to match list 
step 2 - Select a specific odds for a specific match
step 4 - Enter stake at right side €110.00
step 5 - Click on "PLACE BET" button
Expected Result :
1) Show validation message "Maximum stake is €100.00"
2) Should not be able to place a bet


Scenario 5: Stake exceeds user balance
ID: S05
Title : User tries to enter stake value greater than his balanace
Priority : High
Risk Rationale : Balance cannot be negative and its a violation of business rule, also financial loss 
Steps : 
step 1 - Navigate to match list and user balance is €20
step 2 - Select a specific odds for a specific match
step 4 - Enter stake at right side €50.00
step 5 - Click on "PLACE BET" button
Expected Result :
1) Show validation message "Insufficient balance"
2) Should not be able to place a bet



Scenario 6: Odds selection
ID: S06
Title : By default no odds should be selected 
Priority : Medium
Risk Rationale : User may place wrong bet and lose money
Steps : 
step 1 - Navigate to match list 
Expected Result :
1) No odds should be selected for any match
2) No details should be dispalyed on Bet slip



