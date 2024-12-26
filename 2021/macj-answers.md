# Security 1 2021

### Question 1 - Select the correct statement about Encryption. Select one:

#### a. Users of a symmetric encryption scheme publish a symmetric key in the internet in order to receive encrypted messages.
- No a symmetric encryption scheme needs both Alice and Bob to know the value of a secret key, they can then use to encrypt and decrypt a message. If this was an asymmetric scheme, it could refer to public-key encryption where there exists both a public and private key. 

#### b. Encryption protects the integrity of messages exchanged over a network.
- No encryption does not protect the integrity of a message, as there can be several scenarios where an attacker can intercept an encrypted message and alter it, even if they can decrypt it.

#### c. Encryption protects the confidentiality of messages exchanged over a network.
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


#### d. It is secure against an adversary who eavesdrops but cannot solve the Computational Diffie Hellman problem.
- Diffie-Hellman is only secure against a passive adversary, when they cannot solve the computational Diffie Hellman problem, therefore this is the correct answer. 

### Question 3 - See question in pdf as it is a long description

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




### Question 4

#### a.

#### b.

#### c.

#### d.

### Question 5

#### a.

#### b.

#### c.

#### d.

### Question 6

#### a.

#### b.

#### c.

#### d.

### Question 7

#### a.

#### b.

#### c.

#### d.

### Question 8

#### a.

#### b.

#### c.

#### d.

### Question 9

#### a.

#### b.

#### c.

#### d.

### Question 10

#### a.

#### b.

#### c.

#### d.

### Question 11

#### a.

#### b.

#### c.

#### d.

### Question 12


### Question 13

### Question 14

### Question 15

### Question 16

### Question 17

### Question 18

### Question 19

### Question 20