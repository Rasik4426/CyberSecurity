# Cryptography Basics

## Objective

To understand the fundamental concepts of cryptography, including encryption techniques, hashing, digital certificates, SSL/TLS protocols, and cryptographic tools used to secure information.

---

# Introduction to Cryptography

Cryptography is the science of protecting information by converting readable data (plaintext) into an unreadable format (ciphertext). It ensures that sensitive information remains secure during storage and transmission.

Cryptography helps achieve the following security goals:

* **Confidentiality** – Prevents unauthorized access to data.
* **Integrity** – Ensures data has not been modified.
* **Authentication** – Verifies the identity of users and systems.
* **Non-Repudiation** – Prevents denial of performed actions.

---

# Symmetric Encryption

Symmetric encryption is a method where the same key is used for both encryption and decryption of data.

### Working Process

1. Plaintext is encrypted using a secret key.
2. Ciphertext is generated.
3. The same key is used to decrypt the ciphertext back into plaintext.

### Common Algorithms

* AES (Advanced Encryption Standard)
* DES (Data Encryption Standard)

### Advantages

* Fast encryption and decryption.
* Suitable for large volumes of data.
* Efficient resource utilization.

### Disadvantages

* Secure key sharing is difficult.
* If the key is compromised, all encrypted data can be accessed.

### Example

A company encrypts employee records using a single secret key known only to authorized personnel.

---

# Asymmetric Encryption

Asymmetric encryption uses two different keys:

* **Public Key** – Used for encryption.
* **Private Key** – Used for decryption.

### Working Process

1. The sender encrypts data using the receiver's public key.
2. The receiver decrypts the data using their private key.

### Common Algorithms

* RSA (Rivest-Shamir-Adleman)
* ECC (Elliptic Curve Cryptography)

### Advantages

* Secure key exchange.
* Supports digital signatures.
* Better authentication mechanisms.

### Disadvantages

* Slower than symmetric encryption.
* Requires more computational resources.

### Example

Secure email communication using public and private keys.

---

# Symmetric vs Asymmetric Encryption

| Feature   | Symmetric Encryption          | Asymmetric Encryption |
| --------- | ----------------------------- | --------------------- |
| Keys Used | One Key                       | Two Keys              |
| Speed     | Faster                        | Slower                |
| Security  | Lower Key Management Security | Higher Security       |
| Examples  | AES, DES                      | RSA, ECC              |
| Usage     | Bulk Data Encryption          | Secure Key Exchange   |

---

# Hashing

Hashing is the process of converting data into a fixed-length value known as a hash.

Unlike encryption, hashing is a one-way process and cannot be reversed.

### Common Hashing Algorithms

* MD5
* SHA-1
* SHA-256
* SHA-512

### Applications

* Password storage
* Data integrity verification
* Digital signatures
* File verification

### Example

When a user creates a password, the system stores its hash instead of the actual password.

### Advantages

* Fast processing.
* Protects sensitive information.
* Detects unauthorized modifications.

---

# Digital Certificates

Digital certificates are electronic documents used to verify the identity of websites, organizations, and users.

They are issued by a trusted Certificate Authority (CA).

### Components of a Digital Certificate

* Certificate Owner Information
* Public Key
* Digital Signature
* Expiration Date
* Certificate Authority Details

### Benefits

* Website authentication.
* Secure communication.
* Protection against impersonation attacks.

### Example

A website displaying a padlock icon in the browser uses a valid digital certificate.

---

# SSL/TLS

SSL (Secure Sockets Layer) and TLS (Transport Layer Security) are cryptographic protocols used to secure communication over networks.

TLS is the modern and more secure version of SSL.

### Functions of SSL/TLS

* Encrypts transmitted data.
* Verifies server identity.
* Ensures data integrity.
* Protects against eavesdropping attacks.

### Uses

* Secure websites (HTTPS)
* Online banking
* E-commerce transactions
* Email security

### Example

When visiting an HTTPS website, TLS encrypts all communication between the browser and server.

---

# OpenSSL

OpenSSL is a popular open-source command-line tool used for cryptographic operations.

### Common Uses

* Encrypting files
* Decrypting files
* Generating SSL/TLS certificates
* Creating public and private keys
* Verifying digital certificates

### Example Commands

#### Generate RSA Private Key

```bash
openssl genrsa -out private.key 2048
```

#### Generate Public Key

```bash
openssl rsa -in private.key -pubout -out public.key
```

#### Encrypt a File

```bash
openssl enc -aes-256-cbc -salt -in file.txt -out encrypted.txt
```

#### Decrypt a File

```bash
openssl enc -aes-256-cbc -d -in encrypted.txt -out decrypted.txt
```

### Benefits

* Free and open-source.
* Supports numerous cryptographic algorithms.
* Widely used in cybersecurity and secure communications.

---

# Key Learning Outcomes

After completing this task, you should be able to:

✅ Understand the purpose of cryptography.

✅ Differentiate between symmetric and asymmetric encryption.

✅ Explain the concept of hashing and its applications.

✅ Understand the role of digital certificates.

✅ Explain how SSL/TLS secures network communication.

✅ Perform basic cryptographic operations using OpenSSL.

---

# Conclusion

Cryptography is a fundamental component of cybersecurity that protects sensitive information from unauthorized access and modification. Understanding encryption methods, hashing techniques, digital certificates, SSL/TLS protocols, and tools such as OpenSSL provides a strong foundation for secure communication, data protection, and advanced cybersecurity practices.
