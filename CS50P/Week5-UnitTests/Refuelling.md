# Week 5: Unit Tests - Refuelling

## Problem Overview
The "Refuelling" project focuses on validating and formatting fuel gauge levels. It consists of two main parts: a core logic file (`fuel.py`) that converts fractions (like `3/4`) into percentages, and a test file (`test_fuel.py`) that uses `pytest` to ensure the logic handles valid inputs, zero divisions, and value errors correctly.

## Key Concepts Learned
* **Separation of Concerns:** Dividing code into `convert(fraction)` for calculation and `gauge(percentage)` for formatting.
* **Testing Exceptions:** Learning how to use `pytest.raises` to verify that the code correctly handles invalid inputs like `X/Y` where Y is zero or X is greater than Y.
* **Boundary Testing:** Ensuring that percentages at the extreme ends (≤1% and ≥99%) return "E" (Empty) and "F" (Full) respectively.

## Algorithmic Thinking
The testing strategy for this project was to cover four main areas:
1. **Valid Fractions:** Checking if `3/4` correctly returns `75%`.
2. **Boundary Values:** Ensuring `1/100` returns `E` and `99/100` returns `F`.
3. **Zero Division:** Verifying that a `ZeroDivisionError` is raised when the denominator is 0.
4. **Value Errors:** Ensuring a `ValueError` is raised when inputs are not integers or the numerator is greater than the denominator.
