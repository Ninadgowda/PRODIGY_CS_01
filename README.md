# PRODIGY_CS_01
This Python program implements a simple substitution cipher rather than a classic Caesar cipher. In a substitution cipher, each character in the plaintext is replaced by another character from a randomized version of the allowed characters.

Here’s a breakdown of the code and its functionality:

Key Components:

1. Character Set Creation:

The program creates a character set chars that includes a space, all punctuation characters, digits (0-9), and both lowercase and uppercase ASCII letters.

The chars string is then converted into a list for easier indexing.



2. Key Generation (Randomized Substitution):

A copy of chars is created and shuffled using random.shuffle(). This shuffled list is called key and will serve as the "substitution key" that maps each character in the chars list to a new character in the same list.



3. Encryption Process:

The user is prompted to enter a plaintext message to encrypt.

For each character in the plaintext, the program finds its index in the original chars list and replaces it with the corresponding character from the key list.

The resulting string is stored in the cipher_text variable and displayed as the encrypted message.



4. Decryption Process:

The user is prompted to enter a cipher text (encrypted message) to decrypt.

For each character in the cipher text, the program finds its index in the key list and replaces it with the corresponding character from the original chars list.

The resulting string is stored in the plain_text variable and displayed as the decrypted message.




Example Walkthrough:

1. Encryption:

Input: "Hello!"

Suppose the random key generated is: ["@", "1", "A", "B", "C", ..., "z", "0"] (shuffled version of chars).

For each letter in "Hello!", the program looks up its index in chars and finds the corresponding letter in the shuffled key to build the encrypted message.



2. Decryption:

Input (Cipher Text): "T#pp1b"

The program reverses the process by mapping characters in the key back to their original positions in the chars list to recover the plaintext message.




Key Points:

The cipher used here is not a classical Caesar cipher but a substitution cipher where each character is substituted by a random character from a shuffled set.

Unlike Caesar cipher (which shifts letters by a fixed number), this approach uses a completely randomized mapping, making it more difficult to break without knowing the key.

The program provides basic encryption and decryption based on the random key generated at runtime.


Improvements or Considerations:

Key Storage: The key used for encryption (the shuffled list) is not saved between the encryption and decryption processes. In a real-world application, you’d need a way to securely store or transmit the key for decryption.

Security: While this substitution cipher can obscure the message, it's not cryptographically secure by modern standards and can be broken by frequency analysis if enough ciphertext is available.


