# Shuffled-password-generator


A Python script to generate secure, random passwords by combining letters, symbols, and numbers in a customizable format. The generated password is randomized and includes options for the number of each character type.

## Features
- Generates a strong password using:
  - Uppercase and lowercase letters
  - Special symbols
  - Numbers
- Fully customizable — you can specify the number of letters, symbols, and numbers in the password.
- Ensures randomness by shuffling the characters in the password.

## How It Works
1. **Character Selection**:
   - Letters are selected randomly from a predefined list of uppercase and lowercase letters.
   - Symbols are chosen from a set of common special characters.
   - Numbers are randomly picked from digits `0-9`.
2. **Password Construction**:
   - The script appends the specified number of letters, symbols, and numbers to separate lists.
   - Combines all the lists into one and shuffles the characters for added randomness.
3. **Final Output**:
   - Converts the shuffled list into a string and prints the generated password.

## Prerequisites
- Python 3.x



## Customization
You can modify the number of letters, symbols, and numbers in the password by changing the following variables in the script:

nr_letters = 5  # Set the number of letters
nr_symbols = 3  # Set the number of symbols
nr_numbers = 4  # Set the number of numbers

## Code

import random

# Define character sets
letters = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'
symbols = '!@#$%^&*()_+'
numbers = '0123456789'

# Number of each type of character
nr_letters = 5
nr_symbols = 3
nr_numbers = 4

# Lists to hold characters for each type
pass1 = []
pass2 = []
pass3 = []

# Add random letters
for i in range(nr_letters):
    letter = random.choice(letters)
    pass1.append(letter)

# Add random symbols
for j in range(nr_symbols):
    symbol = random.choice(symbols)
    pass2.append(symbol)

# Add random numbers
for k in range(nr_numbers):
    number = random.choice(numbers)
    pass3.append(number)

# Combine all parts into a single list
password_list = pass1 + pass2 + pass3

# Shuffle the password list for randomness
random.shuffle(password_list)

# Convert list to a string
password = ''.join(password_list)

print("Generated Password:", password)
