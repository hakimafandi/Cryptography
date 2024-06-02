This project implements AES-RSA hybrid encryption method integrates the strengths ofboth AES and RSA algorithms to establish a robust security framework for data protection.By leveraging the symmetric encryption capabilities of AES alongside the asymmetricencryption features of RSA, this hybrid approach ensures comprehensive securitymeasures. AES provides efficient and fast encryption of data, particularly suitable for largevolumes, while RSA facilitates secure key exchange and authentication. This combinationoptimally addresses the requirements of modern digital communication systems, offeringa versatile solution for safeguarding sensitive information across various platforms andenvironments.

How to run 
1. Download vs studio code as a programming language
2. Install jupiter notebook on the extension
3. Execute cell on the vs studio code

Step 1 It  will Generate RSA Key Pair.txt
Step 2 Encrypting Key and Plaintext
Step 3 Decrypting Key and Plaintext

The code imports necessary modules from the Crypto library and the base64 module.
The import_rsa_private_key() function takes a private key file path as input. It reads the private key from the file and imports it using RSA.import_key(). The imported private key is then returned.
The decrypt_aes_key() function takes an encrypted AES key and an RSA private key as input. It creates a PKCS1_OAEP cipher object using the RSA private key. The encrypted AES key is decrypted using RSA decryption, and the decrypted AES key is returned.
The decrypt_message() function takes a ciphertext, an AES key, and a nonce as input. It creates an AES cipher object using the key, CTR mode, and the nonce. The ciphertext is decrypted using the cipher, and the decrypted message is returned.
Person B imports the encrypted AES key from the 'encrypted_key.bin' file.
Person B imports the private key from the 'private_key.pem' file using the import_rsa_private_key() function.
The decrypt_aes_key() function is called to decrypt the AES key, passing the encrypted key and the private key. The decrypted AES key is assigned to the variable aes_key.
Person B reads the ciphertext and the nonce from their respective files.
The decrypt_message() function is called to decrypt the ciphertext, passing the ciphertext, AES key (aes_key), and nonce. The decrypted message is assigned to the variable decrypted_message.
The decrypted message is printed.
