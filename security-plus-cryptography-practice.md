# Security+ Section 7: Cryptography Practice

Completed September 28–29, 2026. Published October 4, 2026.

**Result: 32/35 (91.4%).** Original guided multiple-choice practice with immediate feedback, not an official Udemy or CompTIA exam. Questions and original answers recovered from the study conversation.

Missed questions: 4 (key secrecy versus encoding), 6 (substitution versus transposition), and 11 (Diffie–Hellman).

## Question 1

A stolen file is unreadable without the correct decryption key. Which security goal does this primarily support?

A. Availability

B. Confidentiality

C. Accounting

D. Redundancy

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. Confidentiality.**

Encryption protects **confidentiality** by keeping information unreadable to someone without the correct key—even if they steal the file.

- **A. Availability:** Ensures authorized users can access systems and data when needed.
- **C. Accounting:** Records user activity, such as logins and file access.
- **D. Redundancy:** Provides backup components or systems to help maintain availability.

## Question 2

Which term describes studying cryptographic systems to discover weaknesses or recover protected information without the intended key?

A. Tokenization

B. Steganography

C. Cryptanalysis

D. Obfuscation

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. Cryptanalysis.**

Cryptanalysis is the study of cryptographic systems to find weaknesses that could allow someone to recover protected information without knowing the key.

- **A. Tokenization:** Replaces sensitive information with a substitute value, such as replacing a credit card number with a token.
- **B. Steganography:** Hides a message’s existence—for example, concealing text inside an image.
- **D. Obfuscation:** Makes information or code harder to understand without necessarily encrypting it.

**Memory tip:** Crypt**analysis** = **analyzing** cryptography for weaknesses.

## Question 3

Which requirement is **NOT** directly provided by encryption or digital signatures alone?

A. Keeping a website available during a power outage

B. Protecting message confidentiality

C. Detecting unauthorized message changes

D. Authenticating a message’s signer

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. Keeping a website available during a power outage.**

That requires **availability measures**, such as backup power, redundant systems, or failover. Encryption and digital signatures cannot keep a server powered on.

- **B. Confidentiality:** Encryption makes messages unreadable without the appropriate key.
- **C. Detecting changes:** Digital signatures help detect whether signed information was altered.
- **D. Authenticating the signer:** Digital signatures support this when the verification key is reliably linked to the signer.

## Question 4

An attacker knows which encryption algorithm an organization uses. What should still prevent decryption in a properly designed system?

A. Keeping the algorithm’s name confidential

B. Encoding the ciphertext with Base64

C. Hiding the file extension

D. Protecting a sufficiently strong cryptographic key

**My answer: B. Correct answer: D. Result: Incorrect.**

**Not quite—the correct answer is D. Protecting a sufficiently strong cryptographic key.**

A secure encryption system should remain secure even when the attacker knows its algorithm. **The key must stay secret; the algorithm does not need to.**

- **A. Keeping the algorithm’s name confidential:** Security should not depend on hiding how the algorithm works.
- **B. Base64:** This is **encoding, not encryption**. Anyone can decode it without a secret key.
- **C. Hiding the file extension:** Changing or removing `.pdf`, for example, does not protect the file’s contents.

**Memory tip:** Encoding changes the *format*; encryption protects the *information*.

## Question 5

Which statement correctly distinguishes block ciphers from stream ciphers?

A. Block ciphers use no keys; stream ciphers use keys.

B. Block ciphers process fixed-size blocks; stream ciphers combine data with a generated keystream.

C. Block ciphers provide hashing; stream ciphers provide signatures.

D. Stream ciphers always require public and private keys.

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. Block ciphers process fixed-size blocks; stream ciphers combine data with a generated keystream.**

A **block cipher**, such as AES, transforms fixed-size blocks of data. A **stream cipher**, such as ChaCha20, generates a keystream that is combined with plaintext to encrypt it.

- **A:** Both types use keys.
- **C:** Both perform encryption—not hashing or digital signing.
- **D:** Stream ciphers use symmetric keys, not public/private key pairs.

**Memory tip:** Block = chunks of data. Stream = data combined with a keystream.

## Question 6

A cipher replaces each letter with another letter. A different cipher rearranges the letters without replacing them. What are these techniques, respectively?

A. Substitution and transposition

B. Hashing and salting

C. Transposition and substitution

D. Tokenization and encryption

**My answer: B. Correct answer: A. Result: Incorrect.**

**Not quite—the correct answer is A. Substitution and transposition.**

- **Substitution replaces symbols:** For example, shifting each letter forward one position changes `CAT` to `DBU`.
- **Transposition rearranges symbols:** For example, `CAT` becomes `TAC`. The letters stay the same, but their positions change.

Why the other choices are incorrect:

- **B. Hashing and salting:** Hashing produces a fixed-length digest. Salting adds a value to the input before password hashing.
- **C:** These are the correct terms in the wrong order.
- **D. Tokenization and encryption:** Tokenization replaces sensitive data with a substitute value; encryption is the broader process of converting plaintext into ciphertext.

**Memory tip:** **Substitution = substitute. Transposition = change position.**

## Question 7

Two systems use the same secret key to encrypt and decrypt a backup. What type of encryption is this?

A. Asymmetric

B. Public-key

C. Symmetric

D. One-way

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. Symmetric.**

Symmetric encryption uses the **same secret key to encrypt and decrypt** data. AES is a common example.

- **A. Asymmetric:** Uses a mathematically related public/private key pair.
- **B. Public-key:** Another name for asymmetric cryptography.
- **D. One-way:** Describes functions such as cryptographic hashing, which are not designed to be reversed through decryption.

**Memory tip:** Symmetric = same secret key.

## Question 8

Which algorithm is the best choice among these for modern symmetric encryption?

A. DES

B. MD5

C. RC4

D. AES

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. AES.**

**AES (Advanced Encryption Standard)** is a symmetric block cipher that supports **128-, 192-, and 256-bit keys**. It is widely used to protect files, disks, and network traffic.

- **A. DES:** Its 56-bit key is too short to resist modern brute-force attacks.
- **B. MD5:** A hash function, not an encryption algorithm. It also has known collision weaknesses.
- **C. RC4:** An outdated stream cipher with security weaknesses.

**Memory tip:** AES always uses **128-bit blocks**, even when its key is 192 or 256 bits.

## Question 9

What is a major challenge when using symmetric encryption between parties that have never communicated securely?

A. Symmetric encryption cannot protect files.

B. Securely distributing the shared secret key

C. Symmetric encryption requires certificates for every file.

D. Symmetric encryption only works on small messages.

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. Securely distributing the shared secret key.**

Both parties need the same secret key. The challenge is sharing it securely—if an attacker intercepts that key, they could decrypt the protected information.

- **A:** Symmetric encryption can protect files.
- **C:** It does not require a certificate for every file.
- **D:** It efficiently encrypts large amounts of data.

**Memory tip:** Symmetric encryption is fast, but securely sharing the key takes planning.

## Question 10

Alice wants to encrypt a message so that only Bob can decrypt it. Assuming an appropriate public-key encryption scheme, which key should Alice use?

A. Bob’s public key

B. Alice’s public key

C. Bob’s private key

D. Alice’s private key

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. Bob’s public key.**

Alice encrypts the message using **Bob’s public key**, and Bob decrypts it using **his private key**, which he keeps secret.

- **B. Alice’s public key:** Would protect a message intended for Alice to decrypt.
- **C. Bob’s private key:** Should remain with Bob and must not be shared with Alice.
- **D. Alice’s private key:** Is used to create Alice’s digital signatures, not to keep a message confidential for Bob.

**Memory tip:** Encrypt for the **recipient using their public key**; decrypt using their **private key**.

## Question 11

What is the primary purpose of Diffie–Hellman?

A. Hashing stored passwords

B. Issuing digital certificates

C. Establishing a shared secret over an insecure channel

D. Encrypting an entire hard drive

**My answer: B. Correct answer: C. Result: Incorrect.**

**Not quite—the correct answer is C. Establishing a shared secret over an insecure channel.**

**Diffie–Hellman** lets two parties establish a shared secret without sending that secret across the network. They can then derive a symmetric encryption key from it.

- **A. Hashing passwords:** Uses password-hashing functions, not Diffie–Hellman.
- **B. Issuing certificates:** This is the role of a **certificate authority (CA)**.
- **D. Encrypting a hard drive:** Uses symmetric encryption, commonly AES.

**Memory tip:** Diffie–Hellman = key agreement. It needs authentication to protect against an active on-path attacker.

## Question 12

Why might an organization choose elliptic-curve cryptography (ECC) over RSA for a device with limited computing resources?

A. ECC requires no private keys.

B. ECC makes all communication anonymous.

C. ECC is a symmetric cipher.

D. ECC can provide comparable security with smaller keys.

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. ECC can provide comparable security with smaller keys.**

Smaller keys can reduce storage and communication requirements, making **elliptic-curve cryptography (ECC)** useful for devices with limited resources.

- **A:** ECC still uses private and public keys.
- **B:** ECC does not automatically make communication anonymous.
- **C:** ECC is **asymmetric** cryptography, not a symmetric cipher.

**Memory tip:** ECC = strong security with smaller keys.

## Question 13

A secure communication system uses asymmetric techniques to establish keys and symmetric encryption to protect the actual data. What is this called?

A. Steganography

B. Hybrid cryptography

C. Tokenization

D. Key escrow

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. Hybrid cryptography.**

Hybrid cryptography combines **asymmetric techniques for key establishment** with **symmetric encryption for efficient data protection**. TLS commonly uses this approach.

- **A. Steganography:** Hides a message’s existence inside another medium, such as an image.
- **C. Tokenization:** Replaces sensitive information with substitute values.
- **D. Key escrow:** Keeps protected copies of keys with a trusted custodian for authorized recovery.

**Memory tip:** Hybrid = asymmetric key establishment + symmetric data encryption.

## Question 14

A technician computes a SHA-256 hash of a downloaded file and compares it with a trusted publisher’s hash. What is the technician primarily checking?

A. File integrity

B. File confidentiality

C. User authorization

D. System availability

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. File integrity.**

Comparing the file’s SHA-256 hash with a **trusted publisher’s hash** helps verify that the file has not been altered or corrupted.

- **B. Confidentiality:** Hashing does not hide or encrypt the file’s contents.
- **C. Authorization:** Permissions determine who can access a resource.
- **D. Availability:** Concerns whether systems and data are accessible when needed.

**Memory tip:** Hash comparison = check for changes. A matching hash does not prove a file is harmless—only that it matches the trusted reference.

## Question 15

Changing one character in a document produces a dramatically different hash. Which property does this illustrate?

A. Key stretching

B. Reversibility

C. Escrow

D. Avalanche effect

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. Avalanche effect.**

The **avalanche effect** means a tiny change to the input produces a dramatically different hash output. For example, hashing `Hello` and `hello` produces very different results.

- **A. Key stretching:** Increases the computational work needed to derive a key or test password guesses.
- **B. Reversibility:** Cryptographic hashes are designed to be one-way, not reversible.
- **C. Escrow:** Stores protected keys with a trusted custodian for authorized recovery.

**Memory tip:** Small input change → big hash change.

## Question 16

Two different inputs produce the same hash value. What is this called?

A. Replay

B. Salting

C. Collision

D. Key exchange

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. Collision.**

A **collision** occurs when two different inputs produce the same hash value. Secure hash functions make finding such a pair computationally impractical.

- **A. Replay:** Reusing a captured message or authentication exchange to attempt an unauthorized action.
- **B. Salting:** Adding a unique value to a password before hashing to make precomputed attacks less useful.
- **D. Key exchange:** Establishing cryptographic keys between parties.

**Memory tip:** Different inputs + same hash = collision.

## Question 17

Which option is the most appropriate general-purpose cryptographic hash among these?

A. MD5

B. SHA-256

C. DES

D. SHA-1

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. SHA-256.**

SHA-256 is part of the **SHA-2 family** and produces a **256-bit hash**, commonly used for integrity verification.

- **A. MD5:** Has known collision weaknesses, making it unsuitable when collision resistance is required.
- **C. DES:** An outdated encryption algorithm, not a hash function.
- **D. SHA-1:** Also has known collision weaknesses.

**Memory tip:** SHA-256 hashes data; AES encrypts data.

## Question 18

Which statement about digital signatures is correct?

A. The signer signs with their private key; others verify with the signer’s public key.

B. The signer signs with their public key; others verify with the signer’s private key.

C. Everyone uses the same shared secret to verify the signer’s identity.

D. Signing automatically hides the message contents.

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. The signer signs with their private key; others verify with the signer’s public key.**

A digital signature helps verify **who signed the message** and **whether it was altered**, provided the public key is reliably linked to the signer.

- **B:** Reverses the keys’ roles. The private key creates the signature; the public key verifies it.
- **C:** A shared secret is used in techniques such as HMAC, not public-key digital signatures.
- **D:** Signing does not hide the contents. Confidentiality requires encryption.

**Memory tip:** Sign with **private** → verify with **public**.

## Question 19

A recipient verifies a valid digital signature from a trusted sender. Which property does the signature **NOT** provide by itself?

A. Integrity

B. Origin authentication

C. Support for non-repudiation

D. Confidentiality

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. Confidentiality.**

A digital signature does **not hide the message’s contents**. You need encryption to keep the message confidential.

- **A. Integrity:** The signature helps detect changes to the signed message.
- **B. Origin authentication:** It helps verify the sender when the signing key is reliably linked to their identity.
- **C. Non-repudiation:** It provides evidence supporting that the signer signed the message.

**Memory tip:** Signing proves; encryption conceals.

## Question 20

What is a central purpose of public key infrastructure (PKI)?

A. Replacing all symmetric encryption

B. Preventing every type of malware

C. Binding public keys to identities through certificates and trust relationships

D. Hiding all website addresses

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. Binding public keys to identities through certificates and trust relationships.**

**PKI (Public Key Infrastructure)** uses digital certificates, certificate authorities, and related processes to help establish **who a public key belongs to**.

- **A:** PKI works alongside symmetric encryption; it does not replace it.
- **B:** PKI does not prevent every type of malware.
- **D:** PKI does not hide website addresses.

**Memory tip:** PKI helps answer: “Can I trust that this public key belongs to this identity?”

## Question 21

Which description best matches a typical modern TLS connection using certificates and ephemeral key agreement?

A. The server sends its private key to the browser.

B. The browser validates the server certificate, the parties establish shared keys, and symmetric encryption protects application traffic.

C. The certificate encrypts every packet without session keys.

D. The browser hashes all traffic instead of encrypting it.

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B.**

In a typical modern **TLS connection**, the browser validates the server’s certificate, the parties establish shared session keys, and **symmetric encryption protects the application traffic**.

- **A:** The server’s private key stays secret—it is never sent to the browser.
- **C:** The certificate supports authentication; it does not encrypt each packet.
- **D:** Hashing alone cannot keep traffic confidential. Encryption is needed.

**Memory tip:** Authenticate → establish keys → encrypt traffic.

## Question 22

A company requests a certificate for its website. Which action correctly protects its private key?

A. Keep the private key protected and submit a certificate signing request containing the public key and relevant information.

B. Include the private key in the public certificate.

C. Email the private key to every website visitor.

D. Publish the private key in DNS.

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A.**

The company keeps its **private key secret** and submits a **certificate signing request (CSR)** containing its public key and identifying information. The CSR is signed using the private key, but does not include that private key.

- **B:** A public certificate contains the **public key**, never the private key.
- **C:** Sharing the private key with visitors would compromise it.
- **D:** Publishing the private key in DNS would expose it.

**Memory tip:** Public key goes in the request; private key stays protected.

## Question 23

In a PKI, which pairing is correct?

A. CA: stores user passwords; RA: encrypts disks

B. CA: checks firewall logs; RA: revokes user accounts

C. CA: distributes private keys to visitors; RA: signs all web traffic

D. CA: issues certificates; RA: verifies certificate applicants’ identities

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. CA: issues certificates; RA: verifies certificate applicants’ identities.**

A **Registration Authority (RA)** checks the applicant’s identity. The **Certificate Authority (CA)** issues and digitally signs the certificate.

- **A:** Password storage and disk encryption are not these PKI roles.
- **B:** Firewall monitoring and user-account revocation are not their primary functions.
- **C:** A CA does not distribute private keys to visitors, and an RA does not sign web traffic.

**Memory tip:** RA verifies the applicant; CA issues the certificate.

## Question 24

Which item should **NOT** appear in a publicly distributed X.509 server certificate?

A. Issuer information

B. Validity dates

C. The server’s private key

D. The server’s public key

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. The server’s private key.**

The private key must remain protected. Exposing it could allow an attacker to impersonate the server.

- **A. Issuer information:** Identifies the certificate authority that issued the certificate.
- **B. Validity dates:** State when the certificate’s validity period begins and ends.
- **D. Public key:** Is included so others can use it to verify signatures or perform appropriate public-key operations.

**Memory tip:** Certificates share public keys; private keys stay private.

## Question 25

A certificate covers `*.example.com` and has no additional names listed. Which hostname would it normally cover?

A. `example.net`

B. `portal.example.com`

C. `a.b.example.com`

D. `example.com`

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B. `portal.example.com`.**

The wildcard in `*.example.com` normally covers **one subdomain level**, such as `portal.example.com` or `mail.example.com`.

- **A. `example.net`:** A different domain.
- **C. `a.b.example.com`:** Two subdomain levels—the wildcard covers only one.
- **D. `example.com`:** The base domain must be listed separately in the certificate.

**Memory tip:** One wildcard = one level, not the base domain.

## Question 26

Why does a browser typically warn about an otherwise correctly configured self-signed certificate on a public website?

A. It cannot establish a certificate chain to a trusted authority unless that certificate has been explicitly trusted.

B. Self-signed certificates cannot support encryption.

C. Self-signed certificates always contain malware.

D. Their private keys are automatically public.

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A.**

A self-signed certificate is signed by its own private key rather than by a trusted certificate authority. Unless it has been explicitly trusted, the browser cannot establish the usual trusted certificate chain.

- **B:** Self-signed certificates **can support encryption**.
- **C:** Being self-signed does not mean a certificate contains malware.
- **D:** The private key remains private unless someone exposes it.

**Memory tip:** An encrypted connection is not automatically a trusted connection.

## Question 27

Why would an organization keep its root CA offline and use intermediate CAs for routine issuance?

A. To eliminate certificate expiration

B. To make certificates anonymous

C. To avoid using digital signatures

D. To reduce exposure of the root CA’s highly sensitive private key

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. To reduce exposure of the root CA’s highly sensitive private key.**

The **root CA anchors trust** for the certificate hierarchy. Keeping it offline reduces opportunities for compromise, while intermediate CAs handle routine certificate issuance.

- **A:** Certificates still have expiration dates.
- **B:** Keeping the root offline does not make certificates anonymous.
- **C:** Both root and intermediate CAs still use digital signatures.

**Memory tip:** Protect the root; let intermediates handle daily work.

## Question 28

A website’s private key is exposed before its certificate expires. What should happen to that certificate?

A. It should remain trusted until expiration.

B. It should be converted into a wildcard certificate.

C. It should be revoked and replaced using a new key pair.

D. Its public key should be hidden from browsers.

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C. It should be revoked and replaced using a new key pair.**

Once the private key is exposed, an attacker could use it to impersonate the website. **Revoking the certificate** signals that it should no longer be trusted. A replacement certificate must use a **new key pair**.

- **A:** Waiting until expiration leaves the compromised certificate usable.
- **B:** A wildcard certificate would not fix the exposed key.
- **D:** Public keys are intended to be shared; hiding one does not resolve the compromise.

**Memory tip:** Compromised private key → revoke certificate → generate new keys → replace certificate.

## Question 29

Which statement correctly distinguishes CRLs and OCSP?

A. CRLs encrypt certificates; OCSP decrypts them.

B. A CRL is a published list of revoked certificates; OCSP provides certificate-status responses.

C. OCSP replaces the need for a CA.

D. CRLs contain users’ private keys.

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B.**

A **Certificate Revocation List (CRL)** is a published list of revoked certificates. **Online Certificate Status Protocol (OCSP)** provides a status response for a particular certificate, such as good, revoked, or unknown.

- **A:** Neither mechanism encrypts or decrypts certificates.
- **C:** OCSP checks certificate status; it does not replace the certificate authority.
- **D:** CRLs identify revoked certificates, typically by serial number. They never contain private keys.

**Memory tip:** CRL = check a list. OCSP = request a certificate’s status.

## Question 30

An application is configured to accept only a particular expected server public key. What technique is this?

A. Certificate/public-key pinning

B. Password salting

C. Key escrow

D. Tokenization

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. Certificate/public-key pinning.**

With **public-key pinning**, an application checks that the server’s public key matches the one it expects. A different key is rejected even if its certificate would otherwise be trusted.

- **B. Password salting:** Adds a unique value before password hashing.
- **C. Key escrow:** Keeps protected keys with a trusted custodian for authorized recovery.
- **D. Tokenization:** Replaces sensitive data with substitute values.

**Memory tip:** Pinning = “Accept only the identity credential I expect.”

## Question 31

Someone hides a confidential message inside an ordinary-looking image. Which technique is being used?

A. Hashing

B. Asymmetric encryption

C. Certificate chaining

D. Steganography

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. Steganography.**

Steganography hides a message’s **existence**, such as concealing text inside an image. The hidden message can also be encrypted for additional protection.

- **A. Hashing:** Produces a digest used for purposes such as checking integrity.
- **B. Asymmetric encryption:** Protects information using a public/private key pair.
- **C. Certificate chaining:** Connects a certificate to a trusted root through issuing CAs.

**Memory tip:** Encryption hides the meaning; steganography hides the message’s existence.

## Question 32

What makes unauthorized changes to earlier blockchain records detectable?

A. Each block contains everyone’s private keys.

B. All blockchain data is necessarily encrypted.

C. Blocks are linked using cryptographic hashes, with network consensus governing accepted history.

D. A blockchain does not allow new records.

**My answer: C. Correct answer: C. Result: Correct.**

**Correct! C.**

Blockchain blocks are linked using **cryptographic hashes**. Changing an earlier record changes its hash, breaking the existing links with later blocks. **Consensus rules** help determine which history the network accepts.

- **A:** Private keys should remain secret, not be stored in blocks.
- **B:** Blockchain data is not necessarily encrypted; public ledgers can be readable.
- **D:** Blockchains allow new records to be added.

**Memory tip:** Hashes link the history; consensus determines the accepted history.

## Question 33

A password system adds a unique random salt to each password before processing it with a suitable password-hashing function. What is the main benefit?

A. Passwords can now be decrypted by administrators.

B. Identical passwords need not produce identical stored hashes, and precomputed lookup attacks become less useful.

C. Weak passwords become impossible to guess.

D. The salt must replace the password during login.

**My answer: B. Correct answer: B. Result: Correct.**

**Correct! B.**

A **unique salt** makes identical passwords produce different stored hashes. It also prevents attackers from efficiently reusing precomputed lookup tables, such as rainbow tables, across accounts.

- **A:** Hashing is one-way; adding salt does not make passwords decryptable.
- **C:** Weak passwords can still be guessed. Salting does not eliminate password cracking.
- **D:** Users still enter their passwords. The system uses the stored salt when checking them.

**Memory tip:** Salts are unique, not necessarily secret—they can be stored alongside the hashes.

## Question 34

A company replaces stored payment-card numbers with substitute values and maintains a protected mapping to the original values. What is this?

A. Tokenization

B. Hashing

C. Steganography

D. Transposition

**My answer: A. Correct answer: A. Result: Correct.**

**Correct! A. Tokenization.**

Tokenization replaces sensitive data, such as a payment-card number, with a **substitute value called a token**. In this scenario, a protected mapping connects the token to the original number.

- **B. Hashing:** Produces a one-way digest rather than a substitute backed by a recovery mapping.
- **C. Steganography:** Hides a message inside another medium.
- **D. Transposition:** Rearranges the positions of existing symbols.

**Memory tip:** Token = a stand-in for sensitive data.

## Question 35

A trusted custodian retains a protected copy of a decryption key so authorized recovery remains possible if the original is lost. What is this?

A. Certificate pinning

B. Key exchange

C. Salting

D. Key escrow

**My answer: D. Correct answer: D. Result: Correct.**

**Correct! D. Key escrow.**

Key escrow places a protected copy of a cryptographic key with a **trusted custodian** so it can be recovered under authorized conditions.

- **A. Certificate pinning:** Restricts which certificate or public key an application accepts.
- **B. Key exchange:** Establishes cryptographic keys between parties.
- **C. Salting:** Adds a unique value before password hashing.

**Memory tip:** Escrow = trusted safekeeping for authorized recovery.

## Separate matching exercise — 2/5

This supplementary exercise is excluded from the 35-question score and the portfolio's aggregate totals.

| Scenario | My answer | Correct answer |
| --- | --- | --- |
| Payment processor key protection | TPM | HSM |
| Laptop key protection and boot measurements | Secure enclave | TPM |
| Hardware-isolated execution environment | HSM | Secure enclave |
| Displaying only the last four card digits | Data masking | Data masking |
| Making program logic harder to understand | Code obfuscation | Code obfuscation |

Review: Base64 is reversible encoding; protect encryption keys. Substitution replaces symbols, while transposition rearranges them. Diffie–Hellman establishes a shared secret. TPM supports device keys and boot measurements; HSM protects keys and performs cryptographic operations; a secure enclave isolates sensitive computation.
