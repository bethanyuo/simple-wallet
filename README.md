# Ethereum Simple Wallet
This is an implementation of a simple Ethereum wallet in JavaScript, using the [Ethers.js](https://github.com/ethers-io/ethers.js) library. The wallet will hold a single private key along with its associated Ethereum address.

The [Wallet](https://github.com/ethers-io/ethers.js/blob/master/wallet/wallet.js) class in the Ethers.js library holds: private key + address + ability to sign transactions.

## Installation
* ethers.js
```bash
npm install --save ethers
```
## Samples
* Private Key
```
0x495d5c34c912291807c25d5e8300d20b749f6be44a178d5c50f167d495f3315a
```
* Password
```
p@$$w0rd~3
```
* Recipient Address
```
0x7725f560672A512e0d6aDFE7a761F0DbD8336aA7 
```
## New Wallet by Private Key
First, create a function, which by a given private key returns a Wallet instance. The wallet instance has the wallet's private key, address, and functionality to sign. 

## New Random Wallet
Second, create a method that returns a random generated Wallet using `ethers.Wallet.createRandom`. This method creates a random mnemonic using entropy then from the hierarchical node, it derives once and creates a wallet from its private key. The instance stores the mnemonic and the derivation path.

## Save Wallet as JSON
Create a method called saveWalletToJSON, which takes a Wallet instance and a password and returns a JSON V3 Keystore. Use the wallet’s encrypt method.

## Load Wallet from JSON 
Create a method that takes JSON and a password, decrypts the JSON and returns a wallet instance. Use `ethers.Wallet.fromEncryptedJson(json, password)`.

## Sign a Transaction
Create a method that signs a transaction and returns it.

### Module
MI2: Module 3: E2
