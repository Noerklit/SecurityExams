# Security 1 2021

### Question 1 - Select the correct statement about Encryption. Select one:

#### a. Users of a symmetric encryption scheme publish a symmetric key in the internet in order to receive encrypted messages.
- No a symmetric encryption scheme needs both Alice and Bob to know the value of a secret key, they can then use to encrypt and decrypt a message. If this was an asymmetric scheme, it could refer to public-key encryption where there exists both a public and private key. 

#### b. Encryption protects the integrity of messages exchanged over a network.
- No encryption does not protect the integrity of a message, as there can be several scenarios where an attacker can intercept an encrypted message and alter it, even if they can decrypt it.

#### c. Encryption protects the confidentiality of messages exchanged over a network. (Correct answer)
- The goal of encryption is confidentiality, so this is the correct answer!

#### d. A symmetric encryption scheme uses a secret key for encryption and a different key for decryption.
- No the same key is used for both encryption and decryption.

### Question 2 - When executed over an insecure network, under what conditions is the DiffieHellman protocol secure (i.e. an adversary cannot guess the exchanged key except with negligible probability)? Select one:

#### a. It is secure against an adversary who can mount man-in-the-middle attacks and cannot solve the Computational Diffie Hellman problem.
- If the adversary is active (man-in-the-middle), then Diffie Hellman is not secure, as an attacker can tamper with the mssages being sent, fooling Alice or Bob into thinking they've agreed on a shared key, when in actually, it is two different keys the attacker knows. This is because Diffie Hellman does not provide authenticity and integrity.

#### b.It is secure against an adversary who can mount man-in-the-middle attacks but cannot solve the Discrete Logarithm problem, even though it can solve the Computational Diffie Hellman problem.
- This is also false, as an attacker again can trick Alice and Bob into using secrets known to the attacker. Furthermore if an adversary can solve the Computational Diffie Hellman problem, they would be able to break Diffie Hellman, as they would be able to compute g^ab mod p, based on the things that Alice and Bob sends publicly across the network.


#### c. . It is secure against an adversary who eavesdrops but cannot solve the Discrete Logarithm problem, even though it can solve the Computational Diffie Hellman problem.
- If an adversary can solve the Computational Diffie Hellman problem, they would be able to break Diffie Hellman, as they would be able to compute g^ab mod p, based on the things that Alice and Bob sends publicly across the network. Therefore this is false as a passive adversary that can solve the CDH has all the information necessary to compute the secret.


#### d. It is secure against an adversary who eavesdrops but cannot solve the Computational Diffie Hellman problem. (Correct answer)
- Diffie-Hellman is only secure against a passive adversary, when they cannot solve the computational Diffie Hellman problem, therefore this is the correct answer. 

### Question 3 

#### Bent, Inga and Birte are following COVID-19 social distancing measures and self isolating at home, which means they cannot play their weekly game of Bingo. They have internet access but do not trust online game services to implement a fair Bingo game where the numbers are truly randomly chosen. Moreover, they don’t trust each other to pick the Bingo numbers randomly because they might be tempted to cheat. On top of that, they are very security conscious and do not want anybody else to tamper with or learn the outcome of their bingo games. How can Bent, Inga and Birte play their weekly Bingo game over the internet while addressing all of their concerns? Propose a solution, explain why it is secure and describe the security goals it achieves. You can assume the following conditions in your proposed solution:
- The Bingo game we consider starts with each player publicly announcing
25 numbers from 0 to 128. Next, a sequence of random numbers from 0 to
128 are generated. The winner is the first player whose 25 numbers have
appeared in the sequence of random numbers.
- If a player tries to cheat or refuses to execute the steps of the protocol, the
game ends even if no winner has been found. The cheater is given eternal
shame.
- Bent, Inga and Birte have access to a PKI where they can register digital
certificates.




### Question 4 - A large online shop handles thousands of credit card transactions per day. In order to reduce the risk of security breaches and protect their customers, this shop has deployed the TLS protocol on their web servers and enforces that customers can only access their website through this protocol. What security goals does this system achieve? Select one:

#### a. Confidentiality only.
- Whilst TLS does ensure Confidentiality it also ensures Integrity, making this incorrect.

#### b. Integrity and Confidentiality. (Correct answer)
- TLS provides end-to-end encryption, ensuring that nobody apart from the sender and receiver is able to read or modify the data being sent, thus ensuring Integrity and Confidentiality. This is the correct answer.

#### c. Confidentiality and Availability.
- TLS does not protect against an overload on the network, so it will still be susceptible to attacks aiming to shut down the webpage, therefore not ensuring Availability, making this incorrect.

#### d. Integrity only.
- Whilst TLS does ensure Integrity it also ensures Confidentiality, making this incorrect.



### Question 5 - Alice and Bob decide to defeat Eve’s eavesdropping attempts by using a Onetime Pad for achieving encryption with perfect security (after having securely exchanged sufficient amounts of symmetric key information). However, Eve also gets better prepared to eavesdrop on them and gets a quantum computer with unlimited computational power. What attacks can Eve do in this setting? Select one:

#### a. Eve can brute force all keys for certain ciphertexts and obtain information about the messages exchanged between Alice and Bob.
- Brute-forcing OTP keys doesn’t work because for any given ciphertext, every possible plaintext is equally likely without the exact key. Thus, Eve gains no useful information, even with unlimited computational power.

#### b. Eve cannot obtain any information about the messages exchanged between Alice and Bob. (Correct answer)
- This is the correct answer as the OTP ensures perfect secrecy when implemented correctly. Eve cannot extract any information from the ciphertext, regardless of her computational resources, including a quantum computer.

#### c. Eve can recover the one-time pad secret key from the one-time pad public key.
- The OTP does not use a "public key"; it relies on the pre-shared secret key. Eve cannot recover the secret key without compromising the secure exchange method used to share it.

#### d. Eve can decrypt the ciphertexts using her computer.
- Decrypting OTP ciphertexts without the key is impossible, as the OTP provides no exploitable patterns or shortcuts for decryption.



### Question 6 - Alice and Bob share many symmetric encryption keys and a use new key every time they exchange messages encrypted under a Mono-alphabetic substitution cipher. Suddenly they realize that Eve, a Dolev-Yao adversary, has been reading all of their messages even though they are encrypted. How can Eve read these encrypted messages efficiently? Select one:

#### a. Eve brute forces every possible key for every possible ciphertext.
- Whilst this could be done with infinite time or infinite computing power, it is not feasible so this is incorrect.

#### b. Eve has hacked into Bob’s computer and thus can read the plaintext messages after they are decrypted.
- A Dolev-Yao adversary has full control of the network, allowing them to overhear, intercept and synthetize any message, but this adversary does not implicitly have access to the computers of others, making this incorrect. 

#### c. Eve explores frequency analysis attacks to recover the messages since she knows the language Alice and Bob are using. (Correct answer)
- This is the correct answer, as a mono-alphabetic substitution cipher, can usually be broken if the spoken language is known, as some words appear more frequently than others. By analysing messages, and discovering common words, the cipher kan be broken.

#### d. Eve is lucky to guess all messages.
- This is incorrect, as this is statistically improbable.




### Question 7 - Select the correct statement about permissionless Blockchains. Select one:

#### a. Users have to register their public keys in a PKI before executing the blockchain protocol.
- No the fact that it is permissionless, implies that users can join anonymously with their own generated key pairs.

#### b. Any user can join the execution of the blockchain protocol.
- Permissionless blockchains are open to anyone. Any user with access to the internet and the required software can join, validate transactions, and participate in consensus without needing permission or prior approval, making this the correct option.

#### c. For such a blockchain protocol to be secure, it is necessary that more than two thirds of the parties executing the protocol are honest.
- This is incorrect as it is only necessary for 51% to be honest, not 66,66%
- The required proportion of honest participants depends on the consensus mechanism:
- PoW (Proof of Work): Security requires more than 50% of computational power to be controlled by honest miners, not two-thirds.
- PoS (Proof of Stake): Security requirements vary but do not necessarily require two-thirds honest parties. Some protocols like Byzantine Fault Tolerance (BFT) require two-thirds honest nodes, but this is not universal across all permissionless blockchains.

#### d. The protocol terminates at a certain point, when all the users have achieved agreement on the contents of the blockchain.
- Permissionless blockchains do not "terminate" as they are designed to be continuous, allowing new blocks to be added indefinitely.
- Agreement (consensus) is achieved on a block-by-block basis as the chain grows, but the protocol itself never terminates.




### Question 8 - In a MPC (Multi-Party Computation) computation between n parties of a function f(x1, ..., xn) = y where party Pi has an input bit xi for i = 1, ..., n, what statement is correct? Select one:

#### a. The adversary can make the protocol output an arbitrary value y.
- Incorrect, In a secure MPC protocol, the computation ensures correctness even if some parties are controlled by an adversary.
This means the adversary cannot arbitrarily manipulate the output y without breaking the protocol's security assumptions.

#### b. The adversary learns nothing about the honest party inputs.
- If the adversary was passive (follows the protocol, but tries to infer additional information), this would be correct. But if they are active and deviates from protocols, additional things are needed to prevent leakage of input information.

#### c. The adversary only learns the output y. (Correct answer)
- In a secure MPC protocol, the adversary will learn only the final output y, regardless of whether it controls some parties, therefore this is true. 

#### d. The parties compute the output without communicating.
- Communication is essential in MPC. Parties exchange encrypted or otherwise secure messages to collaboratively compute the function $f(x_1.x_2,..,x_n =y)$ while preserving privacy. Without communication, the parties cannot achieve the guarantees of input privacy or correctness. 


### Question 9 - How are confidentiality, authenticity and integrity achieved by the TLS protocol? Select one:

#### a. Confidentiality is achieved with a symmetric encryption scheme, integrity and authenticity are achieved by signing every message exchanged throughout the protocol with digital signatures.
- The only thing incorrect here is that integrity is not achieved with digital signatures, but by the server and client exchanging and verifying MACs over all messages sent so far.

#### b. Confidentiality is achieved with a public key encryption scheme, integrity and authenticity are achieved by signing every message exchanged throughout the protocol with digital signatures.
- TLS does not use a public encryption scheme, and integrity is not achieved through digital signatures.

#### c. Confidentiality is achieved with a public key encryption scheme, integrity is achieved with digital signatures and authenticity is achieved with a MAC.
- TLS does not use a public encryption scheme, and integrity is not achieved through digital signatures, and authenticity is not achieved with a MAC. 

#### d. Confidentiality is achieved with a symmetric encryption scheme, integrity is achieved with a message authentication code (MAC) and authenticity is achieved with digital signatures. (Correct answer)
- This is correct, as Confidentiality is ensured through encryption, integrity is achieved by the server and client exchanging and verifying MACs over all messages sent so far, and authenticity is achieved by signing messages with digital signatures. 


### Question 10

#### a. Passwords that are only 16 characters long can easily be cracked by brute force attacks
- 16 characters is long enough that the permutations make it quite hard to simply bruteforce a code.

#### b. The policy makes an assumption that users will change their passwords but does not actively enforce password changes. (Correct answer)
- This is correct, and is a vulnerability, as always, human error and/or stupidity is a vulnerability.

#### c. Passwords containing numbers and special characters make it easier to build efficient dictionaries that allow for quick guessing of passwords.
- No using special characters makes it harder to build efficient dictionaries as there has to be more total characters in the dictionary.

#### d. Using hashing with salts is not a secure method for storing human readable passwords.
- Incorrect, as hashing with salts is actually a more secure method of storing passwords, as this makes it so that even identical passwords have different salted hashes, because their salts are unique, therefore protecting against Rainbow tables (precomputed tables of hash values for common passwords).



### Question 11 - The following piece of code sends a request to openapi.com and assigns the data in the response to the href on the webpage. To which kind of attack is this piece of code vulnerable? Select one:

```
let a = document.getElementById("myLink");
fetch("openapi.com").then(res => a.href = res.data);
```

#### a. None of the other alternatives.

#### b. XSS

#### c. SQL injection

#### d. Command injection


### Question 12

### Question 13

### Question 14

### Question 15

### Question 16

### Question 17

### Question 18

### Question 19

### Question 20

### Question 21

### Question 22

### Question 23

### Question 24

### Question 25

### Question 26

### Question 27

### Question 28

### Question 29

### Question 30

### Question 31

### Question 32

### Question 33

### Question 34

### Question 35

### Question 36

### Question 37

### Question 38

### Question 39

### Question 40

### Question 41

### Question 42