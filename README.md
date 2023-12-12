# LAB. CRYPTOGRAPHY
## NETWORKS AND INFORMATION SYSTEMS SECURITY

The implementation aligns with the proposed secure communication system. It incorporates:

•	Asymmetric Cryptography: For digital certificates and secure communication (S/MIME).
•	Symmetric Cryptography: AES encryption for group messages using a shared session key.
•	Key Exchange Protocol: Diffie-Hellman for establishing shared secrets among multiple entities.


•	Central Trust Point (Gateway as EntityCA):

The implementation uses EntityCA as the Certificate Authority, which aligns with the require-ment for a central trust point. EntityCA issues certificates to all entities, establishing a trust framework.
Alignment: Yes, but EntityCA is not actively involved in message exchanges; it provides the foundational trust through certificates.

•	Decentralized (P2P) and Private Communication:

The communication between entities (like EntityA and EntityB) is peer-to-peer, with messages encrypted and decrypted directly between entities.
Alignment: Yes, the communication system is decentralized and private, as messages are ex-changed directly.

•	Authentication Before Communication:

Entities authenticate to each other using digital certificates issued by EntityCA. This is implicit in the S/MIME process, where the verification of the signed message also serves as authentica-tion.
Alignment: Partial. While S/MIME provides authenticity of the message sender, explicit mutual authentication processes are not demonstrated.


•	Confidentiality and Integrity of Messages:

S/MIME ensures the confidentiality and integrity of messages between two entities (e.g., EntityA and EntityB). Encryption provides confidentiality, while digital signatures ensure integrity and authenticity.
Alignment: Yes, for two-party communication. However, for group communication using the Diffie-Hellman shared secret, only confidentiality is ensured. Integrity checks for group messages are not explicitly implemented.
![image](https://github.com/fjpiedade/cryptography/assets/82730685/b1ef29e2-90d9-491f-b12a-b8039f79cba1)
