\# Cryptography Basics



\## 1. Introduction



Cryptography uses mathematical techniques to protect information. It supports confidentiality, integrity, authentication, and secure communication.



\## 2. Encryption and Decryption



\*\*Encryption\*\* transforms readable plaintext into ciphertext using an algorithm and a key.



\*\*Decryption\*\* transforms ciphertext back into readable plaintext using the appropriate key.



\### Symmetric Encryption

Symmetric encryption uses the same secret key for encryption and decryption.



Examples include AES (Advanced Encryption Standard).



\*\*Advantages:\*\*

\- Efficient for protecting large amounts of data.

\- Widely used in file and disk encryption.



\*\*Consideration:\*\* The secret key must be protected and shared securely when needed.



\### Asymmetric Encryption

Asymmetric cryptography uses a related public key and private key.



The public key can be shared, while the private key must be protected. Depending on the algorithm and operation, these keys can support encryption, digital signatures, and key establishment.



Examples include RSA and elliptic-curve cryptography.



\## 3. Hashing



A cryptographic hash function converts input data into a fixed-length digest.



SHA-256 produces a 256-bit hash.



Hashing is different from encryption: a secure hash is designed to be computationally infeasible to reverse to recover the original data.



\### File Integrity Verification



If two files have the same SHA-256 digest, this provides strong evidence that their contents are identical, assuming no practical hash collision.



A changed file will normally produce a different hash.



Example command in Kali Linux:



```bash

sha256sum message.txt

```



\## 4. OpenSSL Practical



\### Objective

Encrypt a text file, decrypt it, and compare the original and decrypted files.



\### Environment

Kali Linux with OpenSSL.



\### Algorithm

AES-256-CBC with PBKDF2-based password key derivation.



\### Commands



Create a sample file:



```bash

mkdir -p \~/task1-crypto

cd \~/task1-crypto

printf 'Foundations of Cybersecurity test message' > message.txt

```



Encrypt the file:



```bash

openssl enc -aes-256-cbc -salt -pbkdf2 -in message.txt -out message.enc

```



Decrypt the file:



```bash

openssl enc -d -aes-256-cbc -pbkdf2 -in message.enc -out decrypted.txt

```



Compare the original and decrypted files:



```bash

diff -s message.txt decrypted.txt

```



Calculate their SHA-256 hashes:



```bash

sha256sum message.txt decrypted.txt

```



\### Observed Results



\- The encryption command created `message.enc`.

\- The decryption command recreated the readable content in `decrypted.txt`.

\- The `diff` command reported that `message.txt` and `decrypted.txt` were identical.

\- Both files produced the same SHA-256 hash:



`36c2491a56931f3ca8f56ca05d6bc35b27d00cc246e529c9e7419bf90100a586`



\### Conclusion



The practical demonstrated password-based AES-256-CBC encryption and decryption using OpenSSL. The original and decrypted files were identical, and their SHA-256 hashes matched.



\*\*Security note:\*\* CBC encryption does not authenticate the ciphertext by itself. For real applications, use a suitable authenticated encryption design, such as AES-GCM, with correct key and nonce handling.



\## 5. Safe Cryptography Practices



\- Keep encryption keys and passwords secret.

\- Never store real passwords in public repositories.

\- Use established cryptographic libraries rather than implementing algorithms yourself.

\- Prefer authenticated encryption when appropriate.

\- Verify file integrity when transferring or storing important data.

\- Protect private keys and back them up securely.

