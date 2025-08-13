# Hybrid-Crypto-Steganography

A modern, browser-based application that provides multi-layer security by combining classical cryptography (Hill Cipher), modern block ciphers (SDES), and digital steganography (LSB). This tool allows users to encrypt a message twice before hiding it invisibly within an image file.

Features
Multi-Layer Security: Implements a robust three-step security process:

Hill Cipher Encryption: A classical matrix-based cipher for the first layer of text scrambling.

SDES Encryption: A simplified version of the Data Encryption Standard (DES) to encrypt the output of the Hill Cipher, adding bit-level complexity.

LSB Steganography: Hides the final ciphertext within a cover image by modifying the least significant bits of its pixels, making the data invisible to the naked eye.

Interactive & Modern UI:

A sleek glassmorphism design with an animated gradient background.

Drag-and-Drop file uploads for a seamless user experience.

Live Key Validation with instant visual feedback to ensure keys meet the required format before processing.

Asynchronous Processing with loading spinners on buttons, preventing the UI from freezing during intensive operations.

Client-Side Processing: All operations run directly in the browser using JavaScript. No server is needed, ensuring user data remains private and secure on their local machine.

Cross-Platform: As a web application, it runs on any modern browser (Chrome, Firefox, Edge, etc.) on any operating system (Windows, macOS, Linux).

Technology Stack
Frontend: HTML5

Styling: CSS3 (including Flexbox, Grid, and custom animations)

Logic & Algorithms: JavaScript (ES6+)

APIs: Browser File API, Drag and Drop API, and the HTML Canvas API for image pixel manipulation.

How to Run Locally
No complex setup is required. Follow these simple steps:

Clone or Download: Get the project files (index.html, style.css, script.js) and place them all in a single folder.

Open in Browser: Double-click the index.html file.

Ready: The application will open in your default web browser, ready to use.

How It Works
The application secures your message by passing it through a chain of three distinct security modules.

Text Scrambling (Hill Cipher): Your plaintext message is first transformed using matrix multiplication. This scrambles the letter frequencies, making it resistant to basic analysis.

HELLO → (Hill Cipher w/ Key) → IFMMP (Example)

Bit-Level Encryption (SDES): Each character of the scrambled text is then converted into 8 bits and put through the SDES algorithm. This function performs complex permutations and substitutions on the bits, making the output non-readable and highly secure.

IFMMP → (SDES w/ Key) → ©ñµµÄ (Example non-printable characters)

Concealment (LSB Steganography): The final, fully encrypted message is converted into a binary stream and embedded into the least significant bits of the cover image's pixels. This hides the existence of the message entirely.

Decryption is the exact reverse of this process, using the same keys to unlock each layer.

Example Usage
To Encrypt a Message:
Message: Enter your secret message (e.g., SECRET).

Hill Cipher Key: Enter a valid 4-number key (e.g., 3 3 2 5).

SDES Key: Enter a 10-bit key (e.g., 1010000010).

Image: Drag-and-drop or click to upload a cover image (e.g., a .png file).

Click Encrypt & Hide.

Download the resulting stego-image.png.

To Decrypt a Message:
Image: Upload the stego-image.png you just saved.

Keys: Enter the exact same keys used for encryption (3 3 2 5 and 1010000010).

Click Extract & Decrypt.

The original message, SECRET, will appear in the result box.

License
This project is licensed under the MIT License. See the LICENSE.md file for details.
