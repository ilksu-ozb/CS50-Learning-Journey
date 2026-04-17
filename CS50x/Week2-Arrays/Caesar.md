# Problem Set 2: Caesar

## Problem Overview
This project implements a simple cipher known as "Caesar's Cipher." The program takes a command-line argument (a secret key) and encrypts a plaintext message by shifting each alphabetical character by the given key.

## Key Concepts Learned
* **Command-Line Arguments:** Understanding how to use `argc` and `argv` to get input before the program even starts.
* **Type Conversion:** Using functions like `atoi` to convert strings into integers.
* **Character Manipulation:** Utilizing the `<ctype.h>` library to check for uppercase/lowercase and preserve non-alphabetical characters (like punctuation and spaces).
* **The Modulo Operator:** Implementing the rotation logic to ensure the shift wraps around from 'Z' back to 'A'.

## Algorithmic Thinking
The core challenge was to apply the shift while keeping the case of the letters intact. The formula I used:
`(c + key) % 26`
- `c` is the original character position.
- `key` is the secret key.
