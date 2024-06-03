# Assembly-Interruptions-and-Procedures

## Overview

This assembly program is designed to validate and convert numbers entered by the user in binary, decimal, or hexadecimal formats. 

The program guides the user through a **Menu** with several options, takes input, validates it according to the chosen number system, and then performs the appropriate conversion. If the input is invalid, it prompts the user with an error message.


## DATA Segment

- **msg1, msg2, msg3**: Messages prompting the user to enter numbers in binary, decimal, or hexadecimal formats.

- **oui1, oui2, oui3**: Messages confirming the validity of the entered numbers in binary, decimal, or hexadecimal formats.

- **erreur1, erreur2, erreur3**: Error messages for invalid binary, decimal, or hexadecimal inputs.

- **BString, DString, HString**: Buffers for storing the entered binary, decimal, and hexadecimal strings respectively.

- **MENU**: The main menu displayed to the user with options to choose the number format.

- **mauvaisChoix**: Message displayed when the user makes an invalid choice from the menu.

- **finPrgrm**: Message indicating the end of the program after three invalid attempts.

- **choisirEncore**: Message asking the user if they want to make another choice.

- **DecimalOver**: Warning message for decimal numbers that exceed the maximum value that can be represented in two bytes (65535).

## CODE Segment

The main logic of the program is divided into several parts:

1. **Menu Display and Input Handling**:

    - Displays the main menu and handles user input for choosing the number format.

    - Validates the choice and redirects to the appropriate section for binary, decimal, or hexadecimal input.

2. **Binary Number Handling**:

    - Prompts the user to enter a binary number.

    - Reads and validates the binary input.

    - If valid, converts the binary string to a binary number.

    - Displays a validation message or error message based on the input.

4. **Decimal Number Handling**:

    - Prompts the user to enter a decimal number.
    
    - Reads and validates the decimal input.
    
    - If valid, converts the decimal string to a decimal number.
    
    - Displays a validation message or error message based on the input.

5. **Hexadecimal Number Handling**:

    - Prompts the user to enter a hexadecimal number.
    
    - Reads and validates the hexadecimal input.
    
    - If valid, converts the hexadecimal string to a hexadecimal number.
    
    - Displays a validation message or error message based on the input.

6. **Retry Mechanism**:

    - Allows the user to retry entering a valid choice from the menu up to three times.

    - Ends the program if the user fails to make a valid choice after three attempts.

### Procedures

Several procedures are defined to modularize the program:

1. **LireBinaire, LireDecimal, LireHexa**:

    - These procedures read the input strings for binary, decimal, and hexadecimal numbers respectively.

2. **EstBinaire, EstDecimal, EstHexa**:

    - These procedures validate the input strings for binary, decimal, and hexadecimal numbers respectively.

3. **StringToBinary, StringToDecimal, StringToHexa**:

    - These procedures convert the valid input strings to their respective numerical values.

## Program Flow

1. **Initialization**:

    - The program starts by initializing the data segment and displaying the main menu.

3. **Menu Handling**:

    - The user chooses an option from the menu.

    - Based on the choice, the program redirects to the appropriate section for binary, decimal, or hexadecimal input.

4. **Input Reading and Validation**:

    - The program reads the user input.

    - Validates the input according to the chosen number format.

5. **Conversion and Output**:

    - If the input is valid, the program converts the input string to its numerical value.

    - Displays the conversion result or an error message.

6. **Retry or Exit**:

    - The user is prompted to retry or exit the program based on their choice.

## How to Run the Program

1. **Assemble and Link**:

    - Assemble the program using an assembler like MASM or TASM.

    - Link the object file to create an executable.

2. **Execute**:

    - Run the executable.

    - Follow the on-screen instructions to enter and validate numbers.
