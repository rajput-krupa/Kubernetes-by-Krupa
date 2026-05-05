**When Transfering data over the internet, (confidential info like: authentication details), even if it is encrypted (called *symmetric encryption*), its not safe. The identity and Data is compromised.**

# SSL/TLS
- So instead as a user, we do create a secure connection to the server, so we will create a public and private key.
- Using utility we generate **ssh-keygen** (private & public key)
- Its a seperate key for encryption, as well as a seperate key for decryption. Also called *Assymetric Encryption*.
- This keys are generated through a Utility that is **OpenSSL**.
- User will have the public key and a *symmetric key* and the Server will have the private key.
- User will use the public key to access the symmetric key.

 <img width="661" height="175" alt="Screenshot 2026-05-05 at 5 44 01 PM" src="https://github.com/user-attachments/assets/051e7d88-fdff-4ec4-829b-e1da0b53cc78" />


 # Compromised Ways or Alternative
 As even the above way can be compromised, what if a hacker tries to be a user and gets the publblic key instead.
 So, instead of public and private key, we are using the ***certificates***. 
 Now, browsers can validate whether the certificate was issued to the domain itself.
 
 <img width="611" height="255" alt="Screenshot 2026-05-05 at 5 55 42 PM" src="https://github.com/user-attachments/assets/d64ed980-8583-45f7-8c2b-002669f8cc0b" />


# How is certification Done?
So, the server creates a CSR (Certificate Sign in Request) ---> Request sent to Certificate Authority (Eg: Digicert)---> The CA validates and sends the request to Server back.
Private Certificate is kept to the Server and the Public certificate is sent to the User.


<img width="669" height="210" alt="Screenshot 2026-05-05 at 6 04 31 PM" src="https://github.com/user-attachments/assets/923d16ac-c024-4ab2-93e0-a74dce0235f9" />

<img width="677" height="286" alt="Screenshot 2026-05-05 at 6 18 54 PM" src="https://github.com/user-attachments/assets/dc0c3f71-0bff-4025-8997-40641e6a0f01" />
