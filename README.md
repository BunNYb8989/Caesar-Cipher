# Classification of encryption techniques

<p align="center">
<b>Root User</b>
<br/>
  <img src="Classical encryption Technique.png"/>
<br/>
<br/>
</p>




# Caesar Cipher Works

Substitution Cipher: The Caesar Cipher is a type of substitution cipher where each letter in the plaintext (the original message) is shifted a certain number of places down or up the alphabet.

Shift Key: The number of positions each letter is shifted is called the "key". For example, if the key is 3, then A becomes D, B becomes E, C becomes F, and so on.

Encryption Process:

Choose a shift key (e.g., 3).
Shift each letter in the plaintext by the chosen key.
Wrap around the end of the alphabet if necessary (e.g., with a key of 3, Z becomes C).
Decryption Process:

To decrypt the ciphertext (the encrypted message), shift each letter in the ciphertext by the opposite of the key used for encryption.
For example, if the key is 3, each letter is shifted back by 3 positions (D becomes A, E becomes B, etc.).

<p align="center">
<b>Root User</b>
<br/>
  <img src=""/>
<br/>
<br/>
</p>

# Example
Encryption:

Plaintext: HELLO

Key: 3

Ciphertext: KHOOR

Here’s how each letter is shifted:

H -> K

E -> H

L -> O

L -> O

O -> R

Decryption:

Ciphertext: KHOOR

Key: 3

Plaintext: HELLO

Shifting each letter back by 3:

K -> H

H -> E

O -> L

O -> L

R -> O
