
# RSA Encryption and Decryption Program

## Overview

This project implements RSA encryption and decryption algorithms in C++ for secure data transmission. The program facilitates the generation of RSA key pairs (public and private keys) and allows users to encrypt and decrypt messages securely using these keys.

## Features

- **Secure RSA Encryption**: Developed RSA encryption and decryption algorithms to protect data during transmission.
- **Key Pair Generation**: Automatically generates public and private keys for secure encryption and decryption.
- **End-to-End Encryption**: Messages are encrypted using the recipient's public key and can only be decrypted using the recipient's private key.

## Program Structure

The program consists of the following key components:

1. **RSA Key Generation**: 
   - Generation of a pair of RSA keys (public and private) for each user.
   
2. **RSA Encryption**:
   - Encryption of messages using the recipient's public key.
   
3. **RSA Decryption**:
   - Decryption of received messages using the recipient's private key.

### How RSA Works

- **Key Generation**: RSA uses two large prime numbers to generate public and private keys.
- **Encryption**: A message is encrypted using the public key, which can be shared openly.
- **Decryption**: The encrypted message can only be decrypted by the private key, ensuring data confidentiality.

## Prerequisites

- C++ Compiler (e.g., GCC, MSVC)
- Basic knowledge of cryptography, particularly RSA

## How It Works

1. **Key Generation**:
   - Two large prime numbers are chosen to generate the RSA public and private keys.
   
2. **Message Encryption**:
   - The message to be encrypted is first converted into a numeric form.
   - The encryption formula is:  
     \[
     \text{ciphertext} = (\text{message}^{\text{public key}}) \mod n
     \]
     where \( n \) is part of the key pair.

3. **Message Decryption**:
   - The recipient uses their private key to decrypt the received message:
     \[
     \text{message} = (\text{ciphertext}^{\text{private key}}) \mod n
     \]

### Example Flow

1. Generate RSA keys:
   - Public key (used for encryption)
   - Private key (used for decryption)

2. Encrypt a message:
   - Convert the message into a numeric representation.
   - Encrypt using the recipient's public key.

3. Decrypt the message:
   - Use the private key to decrypt the numeric data back into readable text.

## Usage

1. **Compile the Program**:
   
   Compile the program using your C++ compiler. Example using g++:
   ```bash
   g++ rsa.cpp -o rsa
   ```

2. **Run the Program**:
   Execute the program to generate RSA keys and perform encryption/decryption.
   ```bash
   ./rsa
   ```

3. **Encryption and Decryption Process**:
   - The program will generate a public and private key pair.
   - You can encrypt a message using the public key and then decrypt it using the private key.

## File Descriptions

- `rsa.cpp`: The main C++ file containing RSA key generation, encryption, and decryption functions.
- `rsa.h`: Header file defining the RSA algorithms and helper functions for encryption and decryption.

## Notes

- RSA keys should be large enough (e.g., 2048-bit or more) to ensure security.
- The program assumes basic message encoding (e.g., converting strings to integers), which could be enhanced for more complex use cases.
- The project does not include networking; it's focused solely on RSA encryption and decryption functionality.

## Future Enhancements

- Implement optimized prime number generation for larger key sizes.
- Add support for advanced padding schemes to further enhance security.
