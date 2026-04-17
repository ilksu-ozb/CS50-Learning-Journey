# Week 2: Loops - camelCase

## Problem Overview
The goal of this project was to write a program that prompts the user for a variable name in `camelCase` and outputs the corresponding name in `snake_case`. For example, `preferredFirstName` becomes `preferred_first_name`.

## Key Concepts Learned
* **For Loops:** Iterating through each character of a string to analyze its properties.
* **String Methods:** Using `.isupper()` to detect uppercase letters that signal a new word in camelCase.
* **Conditional Logic:** Dynamically modifying the output based on character case.

## Algorithmic Thinking
The conversion logic follows a simple but effective path:
1. **Input:** Take a string from the user.
2. **Iteration:** Loop through every character in the string.
3. **Detection:** - If a character is uppercase, it means a new word starts. Add an underscore (`_`) and convert the character to lowercase.
    - If it's already lowercase, just keep it as it is.
4. **Result:** Print the modified string without any extra spaces or newlines.
