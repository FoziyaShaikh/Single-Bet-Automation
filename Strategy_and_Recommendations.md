I have selected 2 high value automation test cases: 

1) E2E UI test: a critical user journey
Place a single bet
    -> It's a most critical one as business runs on it.
    -> If it's broken, user can't even place a bet.
    -> It verifies title, stake and odds to place a bet

2) API test: a validation or business rule check via the API directly
Maximum stake validation
    -> If this breaks then user can risk more money and place an invalid bet
    -> More financial risk on both sides - user and business

------------------------------------------------------------------------------------------

Manual test cases:

Some of the test cases are left manually due to below reason:
-> Some of them are filtering and ordering which are more of a exploratory checks.
-> Some of them seems less risky as its pure validation and business rules, as application seems to be at an early stage (ex: potential payout showing wrong value)
-> Some are edge cases like odds value which are static and can be changed from admin side

------------------------------------------------------------------------------------------

Your top 2–3 recommendations if this project were to scale (CI/CD, additional test layers, data
strategy, spec clarifications, etc)

1. **CI/CD Integration**  
   - Automate test runs via GitHub Actions or Jenkins.  

2. **Additional Test Layers**  
   - **API contract tests** to validate schema consistency.  
   - **Performance tests** to ensure betting flow scales under load.
   
3. **Spec Clarifications**  
   - Define exact error message copy for validation failures mainly for stakes. 