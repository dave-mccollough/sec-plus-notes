# Cryptography

- Practice and study of techniques for securing data and communications in the presence of adversaries
- Written or generated codes
- Prevents information from theft, alteration and can be used for user authentication

- **Terms**
  - Cryptography
    - A method of protecting information and communications using codes, so that only those for whom the information is intended can read and process it.
  - Cryptoanalysis
    - A study of methods to defeat codes and ciphers
  - Cryptology
    - Cryptography and cryptoanalysis
  - Cryptovariables
    - Keys may be referred to cryptovariables 

- **Goals of Cryptography**
  - Confidentiality
    - Ensuring information is only accessible to those authorized to have access
  - Integrity
    - Verify that data has not been altered
  - Authentication
    - Verifying the identity of a user, device or entity 
      - Digital certificates
  - Non-repudiation
    - Preventing an entity from denying their involvement in a transaction or activity
    - Digital signatures

- **Algorithm vs Keys**
  - Cryptographic algorithms
    - Methods or procedures used to encrypt or decrypt data
    - Algorithms define how the encryption will be carried out
      - AES - Advanced Encryption Standard
      - RSA - Rivest Shamir Aldeman
      - SHA - Secure Hash Algorithm
    - Strength of algorithm is determined by it's ability to withstand crytoanaylsis and attacks without being flawed
  - Kerckhoffs Principle
    - Guideline for how security systems should be designed
    - A cryptosystem should be secure even if everything about the system is public knowledge except the keys

- **Ciphers**
  - Block ciphers
    - Encrypt data in fixed sized blocks
      - AES uses 128 bit blocks
    - Suitable for processing large amounts of data
  - Stream Ciphers
    - Encrypt data one bit or byte at a time
    - Used when data arrives in a stream
    - Use when device has limited resources

- **Symmetric Encryption**
  - Type of encryption that uses the same key to encrypt and decrypt data
  - The shared key is used to convert plain text into ciphertext and vice-versa
  - Key Sharing
    - Securely sharing the key to encrypt/decrypt data is critical to using symmetric cryptography
  - Speed and efficiency
    - Fast and more efficient than asymmetric keys
    - More suitable for encrypting large amounts of data
    - Simpler mathematical operations when compared to asymmetric cryptography
  - Applications
    - Securing data at rest and in transit 
    - Encrypting files and databases
  - Key Management Challenges
    - Securely storing and sharing keys
  - Security
    - Security depends on key length
      - Longer keys are harder to crack
  - Challenges
    - Key distribution and sharing
    - Scalability issues
      - In large networks the # of required keys can grow to an unmanageable level
    - Key storage and protection
    - Lack of non-repudiation
      - The same key is used by all parties

- **Symmetric Algorithms**
  - Data Encryption Standard (DES)
    - 64 bit block cipher
    - 64 bit key
    - Has been cracked and should not be used
  - Triple DES 
    - Applies DES algorithm 3 times to each block
    - 2 or 3 keys can be used depending on mode
    - Effective strength is really 111 bits
    - Approaching end of life, should be used
  - International Data Encryption Algorithm (IDEA)
    - 64 bit block cipher
    - Variable key size - 64 or 128 bits
    - Key is divided into 52 16 bit subkeys
  - Blowfish
    - 64 bit block cipher
    - Variable key size - 32 -448 bits
  - Skipjack
    - 64 bit block cipher
    - 80 bit key
  - Rivest Cipher 4 (RC4)
    - Widely used by WEP and older implementations of SSL and TLS
      - Stream cipher
      - Variable key size - 40 or 2048 bits
    - Rivest Cipher 6 (RC5)
      - Not widely adopted
      - Variable cipher value - 32, 64, or 128 bits
      - Variable key size - 0 or 2048 bits
    - Rivest Cipher 6 (RC6)
      - Next version of RC5
      - 128 bit block cipher
      - Variable key size - 128, 192, 256 bits
    - Advanced Encryption System (AES)
      - Specification established by NIST in 2001
      - 128 bit block cipher
      - Variable key size - 128, 192, 256 bits
      - Number of encryption rounds is key size dependent
        - 128 bit - 10 rounds of encryption
        - 192 bit - 12 rounds of encryption
        - 256 bit - 14 rounds of encryption

- **Asymmetric Encryption**
  - Public key encryption
  - Uses key pairs - one public and one private key only known to the owner
  - Public key - Can be used to encrypt/decrypt
    - Can be shared with anyone
  - Private Key - Can be used to encrypt/decrypt
    - Kept with owner
  - Encryption
    - Sender encrypts the data using recipients public key
    - Data can only be decrypted by corresponding private key
  - Decryption
    - Recipient uses their private key to decrypt the data
  - Advantages
    - Solves key management challenges
    - Provides a method for digital signatures
  - Disadvantages
    - More computationally intensive
    - Requires careful management of private key
  - Cornerstone of modern internet security

- **Asymmetric Algorithms**
- RSA (Rivest-Shamir-Aldeman)
  - Oldest and most widely used asymmetric algorithms
  - Key sizes - 1024 to 4096 bits
  - Secure data transmission SSL/TLS
- Elliptic Curve Cryptography (ECC)
  - Based on the algebraic structure of an elliptic curve
  - Higher degree of security with smaller key sizes
  - 256 ECC key is considered the equivalent of a 3072 RSA bit key
  - Gaining popularity in mobile and wireless
  - Used in secure messaging, cryptocurrency, and SSL/TLS

- **Hybrid Cryptography**
- Combines Asymmetric and Symmetric encryption
- Asymmetric
  - Key exchange
- Symmetric
  - Data encryption
- More scalable in environments with numerous users
- Widely used for SSL/TLS, email communications, VPNs and cloud storage services

- **Hashing**
- Hash Function
  - Convert an input of any length into a fixed sized string
  - Deterministic
    - Same input produces the same hash value
  - Fast Computation
    - Fast and efficient to compute
  - Pre Image resistance
    - Should be computationally impossible to reconstruct the original input
  - Small changes lead to large differences
    - Minor change in input produces a totally different hash
  - Collision Resistance
    - It should be extremely unlikely for two different input sto produce the same hash value
  - Collision hash
    - Two different inputs create the same hash
      - Sigh of weakness
      - Birthday attack is an example

- **Hashing Algorithms**
- SHA
  - Promoted by NIST
  - Used to produce digital signatures and certificates
- SHA-1
  - Uses 512 bit blocks to produce 160 bit message digest 
  - Deprecated by NIST
- SHA-2
  - SHA-256 processes 512 blocks to produces 256 bit message digest
  - SHA-512 processes 1024 blocks to produce 512 bit message digest
- SHA-3
  - Supports the same modes as SHA-2 and is used as a drop in replacement

- **Digital Signatures**
  - Cryptographic technique used to validate the authenticity of a message, software or digital document
  - Created using a persons private key which is part of their key pair (public and private)
  - Created by running a message through a hash function to create a message digest, then encrypting the digest with the signers private key
  - To verify the signature
    - The recipient uses the senders pubic key to decrypt the signature
    - The recipient runs the same hash function on the original message to generate a message digest
    - If the signature matches, this confirms the message has not been altered
  - Security and reliability
    - Authenticity 
      - Confirm the signature was created by the known sender (non-repudiation)
    - Integrity
      - Ensure the message was not altered in transit
    - Non-repudiation
      - Signer cannot deny the authenticity of their signature on a document since it was created with their private key
  - Digital Signature Standard (DSS)
    - Uses the Digital Signature Algorithm developed by the NSA
    - Uses SHA2/SHA3 with RSA or DSA or ECDSA
    - Standard for US government authentication of electronic documents

- **PKI OB**
  - Public Key Infrastructure
    - Create, manage, distribute, use, store, and revoke digital certificates and public-key encryption
    - PKI facilitates the secure transmission of information for a range of activities
      - Ecommerece
      - Online Banking
      - Confidential email
    - Encrypt and decrypt data using public keys
    - Support the creation and verification of digital signatures
    - Certificate Management - certificates have a defined lifecycle and must be managed

- **SSL/TLS Handshake**
  - Client sends a request to the server for a secure session
  - Sever sends X.509 digital certificate to the client
  - Client receives certificate
  - Client authenticates the server using a known list of certificate authorities
  - Client generates random symmetric key and encrypts using the servers public key
  - Client and server now know the symmetric key and can use SSL encryption process to encrypt and decrypt the information contained in the client request and the server response

- **PKI Process**
  - Components of PKI
    - Digital certificate
    - Certificate authority
      - Manages digital certificates
    - Registration authority
      - Verifier for the certificate authority
    - Validation authority
      - Checks if the certificate is valid
    - Certificate Signing Request
      - Used to obtain a digital certificate from a certificate authority

- **Certificates**
- X.509 Digital Certificate
  - Version number
  - Subject name
    - Common name
    - Distinguished name
  - Subject public key
  - Issuer name
  - Validity period
  - Signature Algorithm ID
  - Serial Number
- Certificate types
  - CA Certificate
    - Grants an organization the ability to be a certificate authority
  - End Entity Certificates
  - Wildcard Certificates
    - Supports multiple subdomains
- Self signed vs third party

- **PKI Verification**
  - Verify the certificate from the CA is valid
  - Trust the CA
  - Check if certificate is not listed on certificate revocation list (CRL) or online certificate status protocol (OCSP)
  - Certificate contains data you are trusting

- **Stenography**
  - Concealing a message, image or file within another message, image or file

- **Blockchain**
  - Distributed or decentralized ledger technology
  - Support for cryptocurrencies or bitcoin
  - Chain of blocks where each block contains a transaction 

- **Salting**
  - Adding a random string of characters to a password or sensitive data before it is hashed

- **Trusted Platform Module (TPM)**
  - Secures hardware by integrating cryptographic keys into devices

- **Secure Enclave**
  - A highly secure space within a device where sensitive data can be stored and cryptographic processes can occur isolated from main operating systems and processes

- **Obfuscation**
  - Disguising data to prevent it from unauthorized access
    - Data masking
    - Tokenization
    - Encryption

- **Tokenization**
  - Substituting sensitive data with non-sensitive equivalents known as tokens
  - Tokens have no meaning or value

- **Key Escrow**
  - Cryptographic keys are stored so under certain circumstances a third party can access them
  - Compliance with law enforcement or business continuity

- **Hardware Security Module (HSM)**
  - Physical or cloud resource that provides cryptographic processing, key generation, storage, and encryption/decryption services