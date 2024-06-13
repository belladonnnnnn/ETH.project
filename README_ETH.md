# ETH1_Project - ETH PROOF: Beginner EVM Course
Presenting a simple Solidity smart contract that represents a token with necessary functions such as token burning and minting.



## Description
This program is a contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This program serves as a compilation of all the things that were taught in the ETH Beginner Course under solidity like having public variables that store the details about your coin, having a mapping of addresses to balances, a mint function that takes two parameters: an address and a value and a burn function.

## Getting started and Code
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ETH!_Project.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;
contract MyToken {

    // public variables here
    string public tokenName = "MANJULA";
    string public tokenAbbrev = "JAISWAL";
    uint public total_Supply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        total_Supply += _value;
        balances[_address] +=_value;
    }

    // burn function
    function burn (address _address, uint _value) public {
      if (balances[_address] >= _value){
        total_Supply -= _value;
        balances[_address] -=_value;
    }
    }

}
```

## Overview
The purpose of this project is to provide users with a practical understanding of various concepts taught in the ETH_Beginner Course on Solidity. This program includes hands-on examples and implementations to reinforce learning and demonstrate the functionality of key Solidity features.
