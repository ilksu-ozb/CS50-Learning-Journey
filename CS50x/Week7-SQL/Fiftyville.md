# Problem Set 7: Fiftyville (SQL Detective)

A theft occurred in the town of Fiftyville, and the only way to find the thief, their accomplice, and the city they escaped to was by querying the town's database. I had to piece together information from crime scene reports, ATM transactions, bakery security logs, and phone calls.

## Key Concepts Learned
* **Relational Databases:** Understanding how different tables (like `people`, `bank_accounts`, and `flights`) connect through "Joins."
* **SQL Queries:** Writing complex `SELECT` statements with multiple `JOIN`, `WHERE`, and `INTERSECT` clauses.
* **Data Analysis:** Filtering through thousands of rows of data to find the intersection of specific events (e.g., someone who was at the bakery AND made a call AND took a flight).

## Algorithmic Thinking (The Investigation Path)
To solve the mystery, I followed a multi-step SQL strategy:
1. **Crime Scene Report:** Started by searching for the theft report at the given location and date.
2. **Witness Interviews:** Queried the `interviews` table to get clues about the bakery's security cameras and ATM withdrawals.
3. **Connecting the Dots:** Used nested queries to find people who:
    - Left the bakery within 10 minutes of the crime.
    - Withdrew money from the ATM on Leggett Street.
    - Made a phone call lasting less than a minute.
    - Took the earliest flight out of Fiftyville the next day.
