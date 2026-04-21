Bug ID : B01
Title : Showing past matches on list
Severity: Critical 
Reproduction Steps : 
step 1 - Navigate to match list 
Expected result
It should only show upcoming matches as heading is also there like "Upcoming Football Matches" 
Actual result
It is showing all matches - past and upcoming
Business Impact: If user missed to see the date then financial lose can happen and invalid bet is placed
Evidence: B01.png


Bug ID : B02
Title : Balance not updated after placing a bet
Severity: Critical 
Reproduction Steps : 
step 1 - Navigate to match list 
step 2 - Select odds to place a bet
step 3 - Enter stake 
step 4 - Click on "PLACE BET" 
step 5 - Repeat from step 2 and enter as stake greater than balance (as its not deducted)
Expected result
It should show updated balance to avoid entering wrong stake value
Actual result
The balance is not updated and user can enter stake more than his balance and place an invalid bet succesfully
Business Impact: Till the app is not refreshed it's not deducting the balance so user can keep on placing a bet which is business rule violation and impact business finance
Evidence: B02.gif 

Bug ID : B03
Title : Odds maximum value not working beyond 10
Severity: High
Reproduction Steps : 
step 1 - Navigate to match list 
step 2 - Select maximum odds greater than 10.00
step 3 - Click "Apply" 
Expected result
User should see odds greater than 10.00 for upcoming matches
Actual result
1) It allows to enter but doesn't apply beyond 10
2) If it's based on available odds then when user tries to enter beyond 10.00 proper feedback should b there
Business Impact: If user wants to place a bet beyond 10 odds then he can't , revenue gets impacted
Evidence: B03.gif

Bug ID : B04
Title : Inconsistent success receipt
Severity: Medium
Reproduction Steps : 
step 1 - Navigate to match list 
step 2 - Select odds to place a bet
step 3 - Enter stake 
step 4 - Click on "PLACE BET" 
Expected result
1) Once placed successfully then it should show Success receipt with Bet ID, Match details, Selection, Stake, Odds, Potential payout, Placement timestamp 
Actual result
1) It is not showing "Selection" field 
2) Wrong payout calcualtion
3) Changes the "Match details" by swapping teams
Business Impact: As details are not displayed proper and incorrect calcualtion , we may lose user's trust
Evidence: B04-1.png and B04-2.png


