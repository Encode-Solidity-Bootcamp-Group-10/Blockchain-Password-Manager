## 2-SmartContract

### 2.1-Deploy Vault Factory Contract

#### Execution

```
ts-node --files scripts/vaultFactoryDeploy.ts
```

#### Console.log

```
Using address 0xF233d122F96fFb3A283E712B4c439cba176C548d
balanceBN 98631915993615608
Wallet balance 0.09863191599361561
Deploying Vault Factory Contract
Awaiting confirmations
Completed
Vault Factory Contract deployed at 0xb4B559447c834C991Cb26FbbDB0B7c170811831F
```

### 2.2-Verify Vault Factory Contract Code at Etherscan

#### Execution

```
npx hardhat verify --network ropsten 0xb4B559447c834C991Cb26FbbDB0B7c170811831F
```

#### Console.log

```
Nothing to compile
No need to generate any newer typings.
Successfully submitted source code for contract
contracts/VaultFactory.sol:VaultFactory at 0xb4B559447c834C991Cb26FbbDB0B7c170811831F
for verification on the block explorer. Waiting for verification result...

Successfully verified contract VaultFactory on Etherscan.
https://ropsten.etherscan.io/address/0xb4B559447c834C991Cb26FbbDB0B7c170811831F#code
```

## Vault

### Requirements Phase 1

- add yourself to a vault
  - this implies storing a private key (encrypted) and public key inside the vault
- get a password
- store a password
- share a password = store for other user

### Requirements Phase 2

- remove yourself from a vault
- [admin] remove other people from the vault
- vote on people joining the vault

## Cryptography

### Generate key pair

```
window.crypto.subtle.generateKey({
  name: "RSA-OAEP",
  modulusLength: 4096,
  publicExponent: new Uint8Array([1, 0, 1]),
  hash: "SHA-256"
}, true, ["encrypt", "decrypt"])
```

### Extract public key from generated key pair

currently: `spki` => base64

possibilities: SubjectPublicKeyInfo (spki), JSON Web Key

### Extract private key from generated key pair

currently: `pkcs8` => base64

possibilities: PKCS#8, JSON Web Key

### Encrypted version of private key
