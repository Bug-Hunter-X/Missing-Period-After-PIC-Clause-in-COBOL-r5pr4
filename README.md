# Missing Period After PIC Clause in COBOL

This repository demonstrates a subtle but potentially problematic error in COBOL: forgetting to add a period (.) after the PIC clause when declaring variables.

## The Bug

In COBOL, data declarations must end with a period.  Forgetting this period can lead to compilation errors or, worse, unexpected runtime behavior, as the compiler might misinterpret subsequent lines of code.

## Example

The `bug.cob` file shows an example of the incorrect code.  Observe the missing period after `PIC X(100)`. 

## Solution

The `bugSolution.cob` file demonstrates the correct code with the necessary periods added to the variable declarations. This ensures that the compiler correctly parses the data descriptions and generates the expected code.

## How to Reproduce

1. Compile `bug.cob` using your COBOL compiler (e.g., GnuCOBOL). Observe the compilation error.
2. Compile `bugSolution.cob`. This will compile successfully.

This example highlights the importance of careful attention to detail when writing COBOL code.  Even seemingly minor errors can have significant consequences.