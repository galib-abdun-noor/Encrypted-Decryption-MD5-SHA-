# Task 1: AES Encryption & Integrity Check
**Implementation Steps:** 

•	**Key Derivation:** A 256-bit AES key is generated from a user-provided password using SHA-256 or MD5.

•	**AES Encryption:** Messages are encrypted using AES-256 in CBC mode with a randomly generated IV (Initialization Vector).

•	**Integrity Check:** The encrypted message is hashed using SHA-256/MD5, and both the encrypted message and hash are stored in a JSON file.

•	**Decryption Process:** The integrity hash is verified before decrypting the message. If the hash does not match, the program alerts the user of possible tampering.

**Test Results:**

**Encryption Success:**

![image](https://github.com/user-attachments/assets/24d09a41-ecda-49fb-9a9a-060c1b96eddf)
 
An encrypted JSON file is created with the information below.

{"username": "foundationofprivacy6413", 

"iv": "6+SiNAUBD1Ohfw7vxLr86A==", 

"encrypted_message": "oawEJlG30UbF2WC3BR5qvYWmtrpkL7zCzHLX3uck7JY=", 

"hash": "b630e283fb916c2c2a8939fa249437dd7812fdca41b5d48f904504292ce6e8d7"}

After decrypting with the same username and password I get the below output.

![image](https://github.com/user-attachments/assets/771eb61d-50f3-47c4-8052-547a5a24398a)
 
Another example with MD5

**Encryption Success:**

 ![image](https://github.com/user-attachments/assets/897d6f32-b5ab-49f6-b119-dc8c00347e87)

**Decryption Success:**

 ![image](https://github.com/user-attachments/assets/fbfafc85-7224-4fff-a2cb-e29b0bfe2314)

# Task 2: SHA-256 Hash Verification of Private Key

**Implementation Steps:**

1.	Read the private_key.pem file.
2.	Compute the SHA-256 hash of the key’s contents.
3.	Compare the computed hash with provided hash values.
4.	Print whether the hash matches or not.

**Test Results:**

**Hash Verification Output:**

 ![image](https://github.com/user-attachments/assets/cb67d822-21f6-4297-8cfc-48061a5f9fd7)


# Task 3: RSA Decryption of Ciphertext

**Implementation Steps:**

•	Read the encrypted message from encrypted_message.txt.

•	Load Alice's private key from private_key.pem.

•	Decode the encrypted message (Base64).

•	Decrypt the message using RSA (PKCS1_OAEP).

•	Print the original message.

 ![image](https://github.com/user-attachments/assets/4e5e041b-fe24-4084-a219-c87c0c0187fd)


