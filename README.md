# DES Implementation in Java

This project is a Java implementation of the Data Encryption Standard (DES), a symmetric-key algorithm for the encryption of digital data.

## Features
- DES key schedule generation.
- Initial and final (inverse) permutation.
- Expansion, permutation, and substitution functions as per DES specification.
- XOR operation for round keys and data.
- DES encryption and decryption functions.

## Getting Started
To run this DES implementation, you will need a Java Runtime Environment (JRE) installed on your machine.

### Prerequisites
- Java Development Kit (JDK) 8 or higher.

### Running the Program
1. Compile the Java program:
   ```
   javac des.java
   ```
2. Run the compiled class with the required arguments. For example:
   ```
   java des <64-bit key> <64-bit data block>
   ```
   Note: Replace `<64-bit key>` and `<64-bit data block>` with appropriate 64-bit binary strings.

## Implementation Details
The DES algorithm implemented here follows the standard DES procedure, which includes:
- A 64-bit key is permuted and reduced to a 56-bit key using the PC1 table.
- The key is then split into two 28-bit halves, which are separately rotated and permuted to generate 16 round keys.
- The data block undergoes an initial permutation, followed by 16 rounds of processing which includes expansion, XOR with round key, substitution using S-boxes, and permutation.
- Finally, an inverse permutation is applied to get the encrypted data.

## Note
This implementation is for educational purposes and demonstrates the basic workings of the DES algorithm. It is not optimized for performance or security in production environments.