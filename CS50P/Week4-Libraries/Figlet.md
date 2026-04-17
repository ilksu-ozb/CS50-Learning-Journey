# Week 4: Libraries - Figlet

## Problem Overview
The goal of this project was to create a program that transforms ordinary text into large, stylized ASCII art fonts using the `pyfiglet` library. The program needed to handle command-line arguments to allow users to specify a particular font or choose one at random.

## Key Concepts Learned
* **External Libraries:** Installing and importing third-party modules (like `pyfiglet`) that aren't part of the Python Standard Library.
* **Command-Line Arguments (`sys.argv`):** Handling user input directly from the terminal to control program behavior.
* **Error Handling:** Validating whether the user provided the correct number of arguments and ensuring the requested font exists in the library.
* **Randomization:** Using the `random` module to select a font when the user doesn't specify one.

## Algorithmic Thinking
The logic flow of the program:
1. **Import** necessary modules: `sys`, `random`, and `pyfiglet`.
2. **Check Arguments:** - If 0 arguments: Pick a random font.
    - If 2 arguments (`-f` or `--font` followed by a font name): Check if the font is valid.
    - Otherwise: Exit the program with an error message.
3. **Input:** Prompt the user for a string of text.
4. **Output:** Convert and print the text in the chosen ASCII font style.
