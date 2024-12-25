# Just notes

### Definitions:

**Keys:**

- In a symmetric key model, Alice and Bob both know the value of a secret key, and they secure their communications using this shared secret value.
- In an asymmetric key model, each person has a secret key and a corresponding public key.

**Confidentiality, Integrity & Authenticity**

- Confidentiality is the security property preventing adversaries from reading our private data. If a message is confidential, then an attacker does not know its contents. Alice uses a key to lock the message in a box, sends the locked box over the insecure channel to Bob, who then uses the key to unlock the box, enabling him to see the message. So basically Alice encrypts message via key, so from plaintext to ciphertext. Encrypted message goes through insecure channel, Bob receives encrypted message and decrypts it via the key, back into plaintext.

- Integritry is the security property that prevents adversaries from tampering with our private data. If a message has integrity, an attacker is unable to change the content of the message without being detected. 

- Authenticity is the security property that lets us determine who created a given message. If a message has authenticity we can be sure that the message was written by the person claiming to have written it. 

- Authenticity and Integritry are very close to each other. To prove a message is authentic you first have to prove it has not been altered, so they go hand in hand.
Usually an algorithm would work something along the lines of: Alice generates a tag or a signature on a message. She sends the message with the tag to Bob. Bob receives the message and tag, verifies that the tag is valid for the mssage, and if the attacker has modified the message, the tag should no longer be valid, and Bob's verification will fail. An attacker should not be able to generate valid tags for their malicious messages.

- A related property that we might want in a cryptosystem is deniability. If Alice and Bob communicate securely, Alice might want to publish a message from Bob and show it to a judge, claiming that it came from Bob. If the cryptosystem has deniability, there is no cryptographic proof available to guarantee that Alice’s published message came from Bob. For example, consider a case where Alice and Bob use the same key to generate a signature on a message, and Alice publishes a message with a valid signature. Then the judge cannot be sure that the message came from Bob–the signature could have plausibly been created by Alice.


### Overview of schemes
![alt text](Images/image.png)
