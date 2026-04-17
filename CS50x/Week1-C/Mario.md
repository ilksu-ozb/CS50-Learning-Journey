# Problem Set 1: Mario 

## Problem Overview
The goal of this project was to recreate the iconic Mario pyramids using ASCII art in C. It focuses on using nested loops to handle dynamic user input for the height of the pyramid.

## Key Concepts Learned
* **Nested Loops:** Using a loop inside another loop to manage rows and columns.
* **Input Validation:** Ensuring the user provides a height within a specific range (e.g., 1-8) using `do-while` loops.
* **Right-Alignment Logic:** Calculating the necessary spaces before the `#` characters to create a right-aligned pyramid.

## Algorithmic Thinking
To build the pyramid, I followed this logic:
1. Get a positive integer `n` from the user.
2. Loop through each row from `1` to `n`.
3. In each row:
    - Print `n - row_number` spaces.
    - Print `row_number` hashes (`#`).
   
