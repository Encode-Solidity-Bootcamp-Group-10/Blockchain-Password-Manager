# Blockchain Password Manager

## About
A Password Manager using the power of the blockchain to securely store your passwords making use of the asymmetric cryptography.

## How it works
- Your login credentials are stored inside a vault which is essentially a smart contract.
- The web frontend will give you the ability to deploy new vaults and edit the user/passwords inside vaults that you own (deployed).
- Due to the open nature of the blockchain, the contents of your encrypted vault can be read by anyone. However it is nearly impossible to derive the decrypted contents.

## Requirements Phase 1

### SmartContract

- add yourself to a vault
  - this implies storing a private key (encrypted) and public key inside the vault
- get a password
- store a password
- share a password = store for other user (optional if inn time)

### Frontend

- Implement the corresponding fronted to connnect all the SmartContract functions

### Cryptography

- Generate keys/pairs
- Extract public key from generated key pair
- Extract private key from generated key pair
- Encrypted version of private key (¿with Metamask?)

![image](https://user-images.githubusercontent.com/1956176/182427604-b34d72e7-8cae-4a1c-a891-8f3a60846e4b.png)
