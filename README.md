# CryptoStar
_Dapp on Ethereum about a simple ERC-721 Token_

## Description
CryptoStar is a notary service that allows you to claim ownership against Star through the [ERC-721](https://docs.openzeppelin.com/contracts/2.x/api/token/erc721) token interface, you can also buy, sell, and, exchange them.

It is published over the Rinkeby Network at [0xF0ee6f4ADBb60c852c9a6af879DB7E5B6073957a](https://rinkeby.etherscan.io/address/0xF0ee6f4ADBb60c852c9a6af879DB7E5B6073957a)
- Token Name: "Gerardo's CryptoStar";
- Token Symbol: "GCS";

---

# Local Development
This project splits in two subprojects:
The backend provide an environment to implement and test the `StarNotary.sol` smart contract, and a frontend that works as a UI for the smart contract.

## Technology Stack
- Truffle v5.1.60
- openzeppelin-solidity v2.4.0
- Solidity v0.5.16
- Node v15.3.0
- Web3.js v1.2.9

## Setting up the development environment
Truffle is a development environment tha manage the contract artifacts.
The right version is included in the `package.json` so you only need to download the dependencies
```shell
$ npm install
```

If you prefer to install Truffle globally, then type: 
```shell
# install truffle globally
$ npm install -g truffle
```

## Build
To generate the contracts artifacts and deploy them to a local blockchain network using truffle, run:
```shell
# start a local network and run the truffle console
$ truffle develop
# creates the bytecode and the ABI
> compile
# deploys the contracts to the local network
> migrate --reset
```

## Run Tests
The test should be run after the contract is migrated 
```shell
$ truffle test
```

## Publish
Publishing the _smart contract_ into a public network requires a wallet with ethereum, to sync a MetaMask
wallet you should create a `.secret` file and add the mnemonic as plain text

```shell
# create the file that will contain the MetaMask mnemonic
touch .secret

truffle migrate --reset --network rinkeby
```

---

# Authors
- [Gerardo Cortés](mailto:gerardo.cortes.o@gmail.com)
