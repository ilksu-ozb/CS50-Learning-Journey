# Problem Set 3: Runoff

## Problem Overview
This project simulates a **Ranked-Choice Voting** system. In this system, voters rank candidates in order of preference. If no candidate receives a majority (>50%) of the first-preference votes, the candidate with the fewest votes is eliminated, and their votes are redistributed to the next preferred candidate in the list.

## Key Concepts Learned
* **Structs:** Defining a `candidate` structure to store multiple data types like `name`, `votes`, and a boolean `eliminated` status.
* **2D Arrays:** Managing voter preferences where `preferences[i][j]` stores the j-th preference of the i-th voter.
* **Logical Flow:** Implementing a multi-step process (Tabulate -> Check Winner -> Find Min -> Eliminate) that repeats until a result is achieved.

## Algorithmic Thinking
To find the winner, I implemented these core steps:
1. **Tabulate:** Count the votes for each voter's highest-ranked candidate who is not yet eliminated.
2. **Victory Check:** Determine if any candidate has more than half of the total votes.
3. **Elimination:** If there is no winner, find the minimum number of votes among active candidates and mark them as eliminated.
