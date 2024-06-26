
# MyToken Solidity Contract

MyToken is a basic Ethereum smart contract written in Solidity that implements a simple token system. It allows for minting and burning of tokens, and tracks the balances of addresses. 

## Description

The MyToken contract provides a simple implementation of a custom token on the Ethereum blockchain. It includes functionalities for minting new tokens, burning existing tokens, and keeping track of token balances for different addresses. 

## Getting Started 

### Installing

To start using the MyToken contract, follow these steps:

* Download the Contract
* Open the MyToken.sol file in your preferred Solidity-compatible IDE, such as Remix.

### Executing Program

#### Deploy the Contract:

* In Remix, select the appropriate Solidity compiler version (0.8.26) and compile the MyToken.sol file.
* Deploy the contract using a JavaScript VM or connect to an Ethereum test network

#### Mint Tokens:

* Call the tknMint function with the recipient address and the amount of tokens to mint:

```
function tknMint(address tknAddress, uint value) public {
    totalSupply = totalSupply + value;
    balance[tknAddress] += value;
}
```

#### Burn Tokens:

* Call the tknBurn function with the address and the amount of tokens to burn, ensuring the address has sufficient balance:
```
function tknBurn(address tknAddress, uint value) public {
    if (balance[tknAddress] >= value) {
        totalSupply = totalSupply - value;
        balance[tknAddress] -= value;
    }
}
```

## Help 

* Ensure you are using the correct Solidity version (0.8.26). If you encounter version-related errors, adjust the version in the pragma solidity directive.

* Verify that addresses and values passed to the tknMint and tknBurn functions are correct and within allowable limits.

## Authors

Harsh Singla
- [@harshsingla](https://github.com/Harshsingla15)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

