
# Blockchain Demo Project 

This project demonstrates the fundamental principles of blockchain technology through an interactive web-based application. Built using HTML, JavaScript, and Material Design components, the application allows users to create, view, and interact with a blockchain in real-time.

## Features

1. **Genesis Block**:
   - The origin block of the blockchain, initialized with default settings and displayed at the top of the chain.

2. **Block Creation**:
   - Dynamically add new blocks to the blockchain.
   - Each block contains:
     - **Data field**: Editable text area for user-defined information.
     - **Nonce field**: Automatically or manually updated during mining.
     - **Hash fields**: Current block hash and previous block hash.

3. **Proof of Work (Mining)**:
   - Simulate the mining process by finding a nonce value that generates a hash matching the difficulty level (leading zeroes).
   - Includes a "Mine" button to start the mining process for a block.

4. **Hash Validation**:
   - Automatically recalculates and validates hashes whenever data or nonce values are modified.
   - Visual indicators (e.g., green for valid hashes and red for invalid hashes) for quick feedback.

5. **Dynamic Blockchain**:
   - Seamlessly chain new blocks to the existing blockchain structure.
   - Automatically propagates hash updates through the chain to ensure integrity.

6. **Responsive UI**:
   - Built using Material Design for an intuitive, clean, and accessible interface.
   - Fully responsive and functional on various device sizes.

## Requirements

- A modern web browser with JavaScript enabled.
- Internet connection to load Material Design and jQuery from the CDN.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. **Open the Application:**
  - Open index.html in a web browser.

## Usage ##

1. **Start with the Genesis Block:**
  - Modify the Stored data field or change the Nonce value.
  - Click the "Mine" button to compute a valid hash for the block.
    
2. **Add New Blocks:**
  - Click "Add next block" to append a new block to the blockchain.
  - Repeat the mining process for each block.
    
3. **Validate Blockchain:**
  - Observe the hash propagation and ensure the entire chain is valid.

## Code Overview ##
### Core Components ###
  - **HTML (index.html):**
    - Provides the user interface, including the genesis block template and dynamic block structure.
    - Includes Material Design styles and JavaScript dependencies.
      
  - **JavaScript (index.js):**
    - Implements the Block and BlockChain classes for blockchain simulation.
    - Handles mining, hash computation, and chain integrity.
      
  - **Styling:**
    - Utilizes Material Design components for a clean and responsive UI.

### Key Classes ###
  - **Block:**
    - Represents an individual block in the blockchain.
    - Includes methods for
        - mining
        - hash computation
        - and UI updates.
  - **BlockChain:**
      - Manages the entire chain of blocks.
      - Handles
          - adding new blocks
          - updating chain integrity
            
### Notable Functions ###
  - Proof of Work:
      - Simulates mining by iterating nonce values until a valid hash is found.
    
  - Hash Validation:
      - Ensures that each block’s hash meets the specified difficulty.
   

## Future Enhancements ##

1. **Persistant Storage:**
    - Add local storage support to save and load blockchain state.
2. **Decentralized Simulation:**
    - Implement real-time peer-to-peer communication for decentralized blockchain simulation.
3. **Enhanced Visualization:**
    - Add animations and graphs to better illustrate blockchain concepts.
4. **Custom Difficulty:**
    - Allow users to set custom difficulty levels for mining

# SJCL (Stanford JavaScript Crypto Library)

This JavaScript file is part of a cryptographic library called **SJCL (Stanford JavaScript Crypto Library)**. It contains implementations of various cryptographic functions such as AES (Advanced Encryption Standard), SHA-256, and other cryptographic primitives.

## Key Sections

### 1. Exception Handling (`sjcl.exception`)
Defines custom error types for different cryptographic exceptions:
- **`corrupt`**: Indicates corrupted data or states.
- **`invalid`**: Represents invalid inputs or parameters.
- **`bug`**: Signals internal errors or bugs in the library.
- **`notReady`**: Indicates that a resource or process is not ready.

These exceptions provide meaningful error messages for issues in cryptographic operations.

---

### 2. AES (Advanced Encryption Standard) Implementation (`sjcl.cipher.aes`)
#### Features:
- **Encryption and Decryption**:
  - Implements the AES algorithm for secure data encryption and decryption.
  - Key schedule initialization and encryption/decryption are handled via the `encrypt` and `decrypt` methods.
- **Key Expansion**:
  - The `O` method generates the key schedule for AES based on the provided encryption key.

---

### 3. Bit Array (`sjcl.bitArray`)
Provides utilities for manipulating bit arrays (arrays of bits). Key methods include:
- **`bitSlice`**: Extracts a slice of bits from a bit array.
- **`extract`**: Extracts a specific range of bits.
- **`concat`**: Concatenates two bit arrays.
- **`clamp`**: Adjusts the bit array length by removing unused bits.

Other helper methods optimize bit array manipulation for cryptographic purposes.

---

### 4. Encodings (`sjcl.codec`)
Implements various encoding and decoding methods:
- **UTF-8** (`sjcl.codec.utf8String`): Converts between bit arrays and UTF-8 strings.
- **Hexadecimal** (`sjcl.codec.hex`): Converts between bit arrays and hexadecimal strings.
- **Base32/32hex/Base64**: Encodes and decodes bit arrays into Base32/Base64 formats.

These encodings ensure compatibility and portability of cryptographic data.

---

### 5. SHA-256 Hashing (`sjcl.hash.sha256`)
#### Features:
- Implements the **SHA-256 hash function**, a widely-used cryptographic hash algorithm.
- **Incremental Updates**:
  - The `update` method allows adding data to the hash in chunks.
  - The `finalize` method completes the hashing process and outputs the result.
- **Hashing Utility**:
  - The `hash` method computes the SHA-256 hash of an input in one step.

---

## Summary
This file is a part of a cryptographic library that provides essential tools for:
- **Encryption**: AES (Advanced Encryption Standard).
- **Hashing**: SHA-256 cryptographic hash function.
- **Bit Array Manipulation**: Utilities for efficient bit-level operations.
- **Encoding Schemes**: UTF-8, Base32, Base64, and hexadecimal encoding.

The **SJCL** library is commonly used in web applications for:
- Password storage.
- Secure communication.
- Cryptographic services requiring secure encryption, hashing, and data handling.

