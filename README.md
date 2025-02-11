# Hybrid_cipher
##  Vigenère + Columnar Transposition3

This repository contains a Python program that implements a **Hybrid Cipher**, combining **Vigenère Cipher** (Substitution) and **Columnar Transposition Cipher** (Permutation) to encrypt and decrypt text. The code can be executed locally or in a Jupyter Notebook environment.

##  About the Code
This program first applies **Vigenère Cipher**, which shifts letters based on a repeating key, and then performs **Columnar Transposition**, rearranging the text based on a key to add further complexity.

##  Logic of the Code
### Encryption:
- The `vigenere_encrypt()` function applies letter shifting based on the Vigenère key.
- The `columnar_transposition_encrypt()` function rearranges the text using a column-based approach.
- The `hybrid_encrypt()` function applies both ciphers sequentially.

### Decryption:
- The `columnar_transposition_decrypt()` function restores the original column order.
- The `vigenere_decrypt()` function reverses the letter shifts.
- The `hybrid_decrypt()` function applies both decryption steps sequentially.

##  Example Execution
```python
plaintext = "SECUREMESSAGE"
vig_key = "STRONGKEY"
trans_key = "COLUMNKEY"

encrypted_text = hybrid_encrypt(plaintext, vig_key, trans_key)
print("Encrypted Text:", encrypted_text)

decrypted_text = hybrid_decrypt(encrypted_text, vig_key, trans_key)
print("Decrypted Text:", decrypted_text)
```

##  How to Run the Code
### Option 1: Run in a Jupyter Notebook
## https://colab.research.google.com/drive/11gRzJMOtsKAGu65s1wcQER9oVab5h6RI?authuser=1

### Option 2: Clone the Repository and Run Locally
Clone the repository using Git:
```sh
git clone https://github.com/manishashetty29/Hybrid_cipher.git
```
Navigate to the project directory:
```sh
cd hybrid-cipher
```
Run the script in Python:
```sh
python hybrid_cipher.ipynb
```

##  Code Explanation
```python
def vigenere_encrypt(plaintext, key):
    # Encrypts text using Vigenère Cipher

def columnar_transposition_encrypt(text, key):
    # Encrypts text using Columnar Transposition

def hybrid_encrypt(plaintext, vig_key, trans_key):
    step1 = vigenere_encrypt(plaintext, vig_key)
    step2 = columnar_transposition_encrypt(step1, trans_key)
    return step2

def hybrid_decrypt(ciphertext, vig_key, trans_key):
    step1 = columnar_transposition_decrypt(ciphertext, trans_key)
    step2 = vigenere_decrypt(step1, vig_key)
    return step2
```
- `vigenere_encrypt(plaintext, key)`: Encrypts using Vigenère shifting.
- `columnar_transposition_encrypt(text, key)`: Rearranges text using columnar transposition.
- `hybrid_encrypt(plaintext, vig_key, trans_key)`: Combines both ciphers sequentially.
- `hybrid_decrypt(ciphertext, vig_key, trans_key)`: Reverses the encryption steps.

##  Features
1) Hybrid encryption using Vigenère and Columnar Transposition
2) Stronger security than individual ciphers
3) Works in Jupyter Notebook & locally
4) Easy to clone and run



