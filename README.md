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
  <img src="Caesar Cipher Works.png"/>
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



# algorithm
<p align="center">
<b>Root User</b>
<br/>
  <img src="chiper algorithm.png"/>
<br/>
<br/>
</p>

in the image the plain text is encrypted by the mod 26 & +3key & the decryption is done by C - k

C = E (p,k) mod 26 = (p+k) mod 26  ENCRYPTION

p = D (C,k) mod 26 = (C-k) mod 26  DECRYPTION

# HERE IS THE CODE 

```
def encrypt(text, shift):
    encrypted_text = ""
    for char in text:
        if char.isalpha():
            shift_base = ord('A') if char.isupper() else ord('a')
            encrypted_text += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
            encrypted_text += char
    return encrypted_text

def decrypt(text, shift):
    return encrypt(text, -shift)

def main():
    print("Caesar Cipher Program")
    choice = input("Do you want to (E)ncrypt or (D)ecrypt?: ").strip().upper()

    if choice not in ['E', 'D']:
        print("Invalid choice. Please choose 'E' for Encrypt or 'D' for Decrypt.")
        return

    message = input("Enter the message: ").strip()
    shift = int(input("Enter the shift value: ").strip())

    if choice == 'E':
        result = encrypt(message, shift)
        print(f"Encrypted message: {result}")
    else:
        result = decrypt(message, shift)
        print(f"Decrypted message: {result}")

if __name__ == "__main__":
    main()

```
